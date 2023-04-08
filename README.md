# MaZe-Space-Collection

A collection of Scipts for Space Engineers, containing:

## Airlock
A simple script to control multiple *airlocks* from a single programmable block.
An airlock consists of two (sets of) *doors* from which only one can be opened at a time. When opening one door, it automaticly closes after a specified amount of time and then the other door opens. Only when the second door is closed, the first one can be opened again.

### Features
- automatic opening/closing airlock
- prevents both doors from being open
- custom door open times
- multiple airlocks per programmable block
- use blockgroup as single *virtual* door

### Usage
To use airlocks on a grid, **one** programmable block must be attached running the script. The doors for the airlock then get detected automaticly **if they are named the right way:** 

Door A: `AirLock_[airlock_name]_1<_[door keepopen time]>`  
Door B: `AirLock_[airlock_name]_2<_[door keep open time]>` 

Where `[airlock_name]` is the name of the airlock (set of two doors) and `<...>` is an optianal suffix specifying the time in milliseconds the door will stay open before closing automaticly.

> #### Example  
> Door A: `AirLock_Hangar_1`  
> Door B: `AirLock_Hangar_2_2000`



After adding / renaming a new door, the **script has to be reloaded** by pressing "run script" inside the programmable block.

Instead of a single door, a block group of doors can be used instead by naming it as specified above. This can be usefull for airtight hangar doors.

