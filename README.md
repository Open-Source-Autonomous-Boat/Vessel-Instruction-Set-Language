# Vessel Instruction Set Language (VIS)
A custom Gcode like language for storing and transmitting instructions for the vessel's mission

## Command Sets

| Letter  | Meaning |
| ------- | ------- |
| C | Direct vessel command such as return to home or change power mode |
| W | Waypoint command such as set or modify waypoint |
| D | Waypoint command such as set or modify waypoint |
| * | Checksum. Used to check for communications errors. |
| Foo | Foo |


## List Of Commands

| Command | Parameters |
| ------- | ---------- |
| W1 | Set waypoint |
| W2 | Modify waypoint |
| * | Checksum |
| Foo | Foo |


# Commands

## C Commands

## W Commands

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

## D Commands
