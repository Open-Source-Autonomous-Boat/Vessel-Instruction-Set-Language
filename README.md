# Vessel Instruction Set Language (VIS)
A custom Gcode like language for storing and transmitting instructions for the vessel's mission

## Instruction Sets

| Letter  | Meaning |
| :-----: | ------- |
| [C](#c-instructions) | Direct vessel instruction such as return to home or change power mode |
| [W](#w-instructions) | Waypoint instruction such as set or modify waypoint |
| [D](#d-instructions) | ... |
| [U](#u-instructions) | Custom user defined instructions |
| [\*](#-checksum) | Checksum. Used to check for communications errors. |
| Foo | Foo |


## List Of Instructions

| Instruction | Action/Meaning |
| :-----: | ---------- |
| **C Instructions** |  |
| **W Instructions** |  |
| [W1](#w1) | Set waypoint |
| [W2](#w2) | Modify waypoint |
| **D Instructions** |  |
| **U Instructions** |  |
| **Other Instructions** |  |
| * | Checksum |
| Foo | Foo |


# Instructions


## C Instructions


## W Instructions


### W1

### Parameters
[Lat],[Long],(Waypoint Number \*Apend to end of sequence)

### Usage
W1,43.627,22.891,6;


### W2

### Parameters
[Lat],[Long],(Waypoint Number)

### Usage
W1,43.627,22.891,6;


## D Instrusctions


## U Instrusctions


## * Checksum
