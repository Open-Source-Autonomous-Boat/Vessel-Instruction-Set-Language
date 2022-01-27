# Vessel Instruction Set Language (VIS)
A custom Gcode like language for storing and transmitting instructions for the vessel's mission

## Table of Contents

1. [Instruction Groups](#instruction-groups)
2. [List Of Instructions](#list-of-instructions)
3. [Instructions](#instructions)

## Instruction Groups

| Letter  | Meaning |
| :-----: | ------- |
| [C](#c-instructions) | Direct vessel instruction such as return to home or change power mode |
| [H](#h-instructions) | File parameters and header information |
| [W](#w-instructions) | Waypoint instruction such as set or modify waypoint |
| [D](#d-instructions) | Data instructions |
| [U](#u-instructions) | Custom user defined instructions |
| Foo | Foo |


## List Of Instructions

| Instruction | Action/Meaning |
| :-----: | ---------- |
| **C Instructions** |  |
| [C1](#c1) | Set navigation mode |
| **H Instructions** |  |
| [H1](#h1) | Set instuction file type |
| **W Instructions** |  |
| [W1](#w1) | Set waypoint |
| [W2](#w2) | Remove waypoint |
| **D Instructions** |  |
| [D1](#d1) | Set command preset |
| [D2](#d2) | Remove command preset |
| **U Instructions** |  |
| **Other Instructions** |  |
| Foo | Foo |


# Instructions


## C Instructions

### C1
Set navigation mode

#### Parameters:
[Mode Number]

#### Usage:
`C1,2;`


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


## W Instructions


### W1

Set waypoint

#### Parameters:
(Waypoint Number \*Append to end of sequence),[Lat],[Long],[Radius],(CMD1 Index),(CMD2 Index)

#### Usage:

- `W1,7,43.627,122.891,40;`
- `W1,,28.140,78.329,60,1,3;` // Append to end of sequence and set commands

---

### W2

Remove waypoint

#### Parameters:
[index]

#### Usage:

`W2,6;`


## D Instrusctions

### D1

Set command preset

#### Parameters:
[Command Index],[Command 1],(Command 2),(Command 3),(Command ...)

#### Usage:

`D1,3,"W1,7,43.627,122.891,40";`
`D1,3,"W1,7,43.627,122.891,40","W2,1";` // Multable commands

---

### D2

Remove command preset

#### Parameters:
[Command Index]

#### Usage:

`D2,6;`


## U Instrusctions
U instructions are reserved for users to define as custom instructions
