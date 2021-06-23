# Vessel Instruction Set Language (VIS)
A custom Gcode like language for storing and transmitting instructions for the vessel's mission

## Instruction Groups

| Letter  | Meaning |
| :-----: | ------- |
| [H](#h-instructions) | File parameters and header information |
| [C](#c-instructions) | Direct vessel instruction such as return to home or change power mode |
| [W](#w-instructions) | Waypoint instruction such as set or modify waypoint |
| [D](#d-instructions) | ... |
| [U](#u-instructions) | Custom user defined instructions |
| [\*](#checksum) | Checksum. Used to check for communications errors. |
| Foo | Foo |


## List Of Instructions

| Instruction | Action/Meaning |
| :-----: | ---------- |
| **H Instructions** |  |
| [H1](#h1) | Set instuction file type |
| **C Instructions** |  |
| [C1](#c1) | Set navigation mode |
| **W Instructions** |  |
| [W1](#w1) | Set waypoint |
| [W2](#w2) | Modify waypoint |
| **D Instructions** |  |
| **U Instructions** |  |
| **Other Instructions** |  |
| * | Checksum |
| Foo | Foo |


# Instructions


## H Instructions

### H1
Set instuction file type

#### Parameters:
[Type Number]

| Type Number | Type |
| :-----: | ---------- |
| 0 | Vessel mission instructions file |
| 1 | Instructions message |
| 2 | Data message |

#### Usage:
H1,0;


## C Instructions

### C1
Set navigation mode

#### Parameters:
[Mode Number]

#### Usage:
C1,2;


## W Instructions


### W1

Set waypoint

#### Parameters:
[Lat],[Long],(Waypoint Number \*Apend to end of sequence)

#### Usage:
W1,43.627,22.891,6;

---

### W2

Modify waypoint

#### Parameters:
[Lat],[Long],(Waypoint Number)

#### Usage:
W1,43.627,22.891,6;


## D Instrusctions


## U Instrusctions


## Checksum
