# The Turing Machine

This simple automaton is a Turing-complete model of computation.

Many decades ago I wrote my first ever program for just such a machine, implemented on an old mainframe by an unknown programmer. My friends and I loved playing with it. Now, you can play with it too.

The following program will find an icecream anywhere on the tape.

```JavaScript
1:E-31-2 // If the caret is over 1, go to command 31, else go to command 2
2:L // Move caret left
3:E-31-4 // If the caret is over 1 (or an icecream ;), go to 31, else go to 4
4:L // Move caret left
5:E-31-6
6:1 // Write 1 (or an icecream)
7:R // Move caret right
8:R
9:R
10:E-26-11 // If icecream, then #26, else #11
11:1 // Write 1 (or an icecream)
12:L // Move caret left
13:E-14-12
14:0
15:L
16:E-21-17
17:1
18:R
19:E-20-18
20:0-9
21:R
22:E-23-21
23:0
24:L
25:E-31-24
26:L
27:E-28-26
28:0
29:R
30:E-31-29
31:STOP // Finish execution
```