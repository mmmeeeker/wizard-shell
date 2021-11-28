# :wizard: shell

Shell extended from a university project in CS33 @ Brown.
Relatively rudimentary w.r.t. features, but could hypothetically 
be daily-driven, so to speak; was mainly written for fun/ out of interest.

Features naive command completions, aliasing, and history, amongst some 
others (whose implementations I would also describe as naive). 


TODO

- HashTable: Need to redo this structure to be specific to my use case, since it currently works
    best with basic data types, but I intended to use them with function pointers. This logic is 
    going to be separated into aliasing and builtins, since the uses are different. The generic 
    things will remain the same, but e.g. I don't want the `get` function to return void ptrs, since
    the casting is obviously problematic.
- Aliasing: The HT structure seems sound. This feature just needs to be implemented in whole.
    In between retrieving the buffer line and tokenizing, there will be a
    "resolve_alias_and_shortcuts" to, well, resolve the aliases and shortcuts. For now, both
    will need to be standalone tokens, seperated by spaces as usual.
    e.g. expect "rm *" to work, but not "rm *.c" -- the latter will, for now, generate a "file
    not found" error. 
 - Coloring: going to make the splash and prompt look a bit nicer. TERM colors are not the most
     vibrant/ conducive to a good graphic design, however.
