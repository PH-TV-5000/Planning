---- Brainstorming ----
1st idea:
    The system will be simulated at a high level using an object (to represent the hardware system and OS)
    and the execution will be done by calling the objects methods. The methods will handle all the delays etc

2nd idea:
    Same as the first idea except seperate the hardware and the OS objects
    

2nd idea will be the way to go I feel

The way it would work is we have the hardware level which effectively provides all the hardware states etc,
but also provides all the methods to do CPU level instructions. Its interface will consist of methods that
will resemble assembly opcodes
The OS level will provide all the other functions, providing both a low and high-level method to program
and use the system.

Will have a main class for the hardware system, possibly with other class instances (representing different, supporting hardware modules) stored in member variables.
The system will define all the needed methods to drive the system, providing a simple interface allowing it to be driven by an OS, interpreter, or some other mechanism.
The system will also likely have an OS allowing it to be used with out a cart inserted.

The functions that will need to be provided are sorted into the following categories:
Memory, Drawing, Math, Comparison, Branching, I/O, Cart, Misc (to be expanded on as needed)
Please note: This is hardware system level features, not library or OS level.

Memory:
    getByte
    setByte
    -- Possibly get or set a specified length of memory (more than a byte)

Drawing:
    blitDisplay
    
Math:
    add and sub
    mult and div
    modulo
    shift left right
    rand

Comparison:
    greater less than
    greater than equal
    less than equal
    equal to
    not and or xor

Branching:
    jump
    call
    return

I/O:
    

Cart:
    

Misc:
    nop
The OS level system will have commands in these categories:
Drawing, Branching, Math, Memory, I/O, Cart, Misc (To be expanded on as needed)

Memory:
    

Drawing:
    
    
Math:


Comparison:
    

Branching:


Control Flow:


I/O:
    

Cart:
    

Misc:
    delayCycles


Struct PHTVPixel:
    uint16_t R : 5
    uint16_t G : 5
    uint16_t B : 5

Class PHTVSystem:
    Member Variables:
        uint16_t displayArray[70][70]
    Methods:
        jadsgl
