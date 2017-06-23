# Regular expresions

Goal: Create patterns that match whole expressions

## Theory
. => match anything but a new line

\s => any white space

\d => digits

\w => a-z ,0-9



## Examples
\s.. => space followed by 2 chars or spaces

\d{1,8} => numbers who has between 1 and 8 digits, for example 2343

[ABC] => one time  A, B, or C

A+ => from 1 to infinite A's

a* => from 0 to infinite A's (makes this value optional)
