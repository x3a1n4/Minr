# TeraRabbits (v1.0.1)

Hey! Thanks for checking out the repo. This is a Minr (zero.minr.org) script that implements worldedit features I like, so that I don't need to keep bothering mods to //smooth for me

- [TeraRabbits (v1.0.1)](#terarabbits-v101)
  - [How to Use](#how-to-use)
    - [Limitations](#limitations)
  - [Features](#features)
    - [Patterns](#patterns)
    - [Brushes](#brushes)
    - [Selections](#selections)
    - [Selection Tools](#selection-tools)
    - [Clipboard](#clipboard)
    - [Miscelaneous](#miscelaneous)
  - [Known Bugs](#known-bugs)
  - [Future Ideas](#future-ideas)
  - [Far Future Ideas](#far-future-ideas)

## How to Use
To use this script, you'll want to bind your favourite block (or entity) with `teraRabbits::enableClickHandlerWrapper()`. This is the entry point to the module, and is independant of the rest of teraRabbits. 

By default, teraRabbits acts as a replace/paint mode for building, similar to Axiom's (including block type replacement). By naming items, you can invoke teraRabbit's suite of tools! Make sure to embed any size arguments within square brackets, e.g `Sphere [4]` makes spheres with a radius of 4.

### Limitations
+ Tools have a max size of `6`
+ Selections have a max block limit of `1000`
+ The player must be in creative mode to use
+ Tools can only edit blocks inside regions that the player is a member of

## Features
### Patterns
| Item Name            | Command Details                                              |
|----------------------|--------------------------------------------------------------|
| `Set Single Pattern` | Sets the block that you're looking at to the active pattern. |

### Brushes
| Item Name        | Command Details                                                             |
|------------------|-----------------------------------------------------------------------------|
| `Sphere [size]`  | Creates a sphere of size `[size]`, using the active pattern                 |
| `Paint [size]`   | Applies the active pattern to all non-air blocks within a radius of`[size]` |
| `Erase [size]`  | Erases a sphere of size `[size]`                                            |
| `Smooth [size]`  | Smooths out terrain in a radius of `[size]`                                 |
| `Pull [size]`    | Pulls terrain towards the player in a radius of `[size]`                   |
| `Flatten [size]` | Flattens terrain around the targeted block in a radius of `[size]`          |

### Selections
| Item Name       | Command Details                                                     |
|-----------------|---------------------------------------------------------------------|
| `Cuboid Select` | Similar to worldedit's //sel cuboid, selects a cube from two points |
| `Cuboid Extend` | Extends the currently selected cube to incorporate the target block |

### Selection Tools
| Item Name   | Command Details                                                          |
|-------------|--------------------------------------------------------------------------|
| `Set`       | Set all blocks in selection to the active pattern                        |
| `Replace Air`       | Replace all air blocks in selection to the active pattern                        |
| `Stack [n]` | Stack the current selection `[n]` times, in the direction you are facing |

### Clipboard
| Item Name | Command Details                                                    |
|-----------|--------------------------------------------------------------------|
| `Copy`    | Copy all blocks in selection to clipboard, from the targeted block |
| `Paste`   | Paste all blocks in clipoard (except air) at the targeted block    |

### Miscelaneous
| Item Name      | Command Details                                                                                                         |
|----------------|-------------------------------------------------------------------------------------------------------------------------|
| `Undo`         | Undo the previous tool action                                                                                           |
| `Spawn Rabbit` | Spawn an invisible, no-AI soundless rabbit at the target block. Fun fact: this was the original purpose of this script!|
| `Show Rabbits` | Show all nearby invisible rabbits |
| `End`          | End teraRabbits, and return to regular creative mode                                                                    |

## Known Bugs
[None at the moment!]

## Future Ideas
These are some ideas that I have for the future. They may or may not be implemented, roughly in order of listing
+ Gradients
  + I've got the block colour data, it's just a matter of using it. I'd love to add darken/lighten brushes or shadow tools at some point
+ Global Masks
  + Currently not implemented whatsoever, but a nice-to-have
+ More Patterns
  + Would love to add random weighted and simplex
+ Flood
  + Water is a pain to build with, sometimes
+ Curves
  + Selection curves such as beziers and catenaries would be great
+ Book Schematics
  + You can _theoretically_ encode schematic information in a minecraft book. Would be useful for asset painting.

## Far Future Ideas
These are some ideas that may actively be bad. More here as archival than anything
+ Smooth Snow
  + My single favourite tool, perhaps ever
+ WFC