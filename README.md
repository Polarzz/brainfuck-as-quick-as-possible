# brainfuck-as-quick-as-possible 
[Brainfuck](https://en.wikipedia.org/wiki/Brainfuck) is an esoteric programming language created in 1993 by Urban Müller and is extremely minimalistic, it only consists of 8 instructions. <br>

`+-><[].,`

Before we begin I would like you to have a look at brainfucks 'hello world' (short):

```brainfuck

+[-[<<[+[--->]-[<<<]]]>>>-]>-.---.>..>.<<<<-.<+.>>>>>.>.<<.<-.

```

Don't worry you will understand what is going on here in just a minute. <br>

Brainfuck uses 'cells' to store data. Each cell will store an integer, which represents an ascii character. <br>

You can move between cells using `<` and `>`

`>` Moves up one cell and `<` moves down one cell.

`+` and `-` are used to manipulate the data stored within each cell, `+` adds one to the cell and `-` subtracts one.

Lets write a simple program:

```bf

++>+++

```

This program will add 2 to the first cell (cell 0) and then move up to the second cell (cell 1) and add 3 to it. <br>

You may be it would take a while to reach the value of any meaningful ascii character using on `+` and `-` so I will show you the next two instructions, `[` and `]`.
