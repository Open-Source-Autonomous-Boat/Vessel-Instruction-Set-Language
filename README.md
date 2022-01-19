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
| [W](#w-instructions) | Waypoint instruction such as set or modify waypoint |
| [D](#d-instructions) | Data instructions |
| [U](#u-instructions) | Custom user defined instructions |
| Foo | Foo |


## List Of Instructions

| Instruction | Action/Meaning |
| :-----: | ---------- |
| **C Instructions** |  |
| [C1](#c1) | Set navigation mode |
| **W Instructions** |  |
| [W1](#w1) | Set waypoint |
| **D Instructions** |  |
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
C1,2;


## W Instructions


### W1

Set waypoint

#### Parameters:
(Waypoint Number \*Append to end of sequence),[Lat],[Long],[Radius],(CMD1 Index),(CMD2 Index)

#### Usage:
W1,7,43.627,122.891,40;
W1,,28.140,78.329,60,1,3; // Append to end of sequence and set commands

---

### W2

Foo

#### Parameters:
[foo],[foo],(foo)

#### Usage:
W1,foo,foo,foo;


## D Instrusctions


## U Instrusctions
U instructions are reserved for users to define as custom instructions
