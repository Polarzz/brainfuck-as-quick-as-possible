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

`[` starts a loop and `]` indicates the end of a loop. <br>
Loops in brainfuck will execute all code inside of them as long as the cell which was being used when the loop started is not 0. <br>
To put it into C:

```c
while(cells_value != 0){
  // code to run
}
```

Now we can multiply.

```bf
++++++ First number is 6

[ start the loop
- take away one from the first number every loop
> move up to the next cell
++++++++++ Second number is 10
< go back to the first cell
this code will execute 6 times meaning 6x10
] end the loop
> go the cell containing our answer
+++++ Add 5
. Now you gaven't seen this yet have you?
```

Or just: `++++++[->++++++++++<]>+++++.`

`.` Will print an ascii character based upon the value of the current cell, so in our example the value was 60, we added 5 so we had a value of 65. <br>
We then print a character based upon this value which is "A" as 65 is ascii for "A".

And finally `,` will ask for one byte of input from the user and store its ascii value in the current cell.

```brainfuck
,.
```

So if you press A the cells value will be set to 65. <br>

And incase you didn't realise already any character that is not an instruction will be ignored.

```
++++++++++[>+>+++>+++++++>++++++++++<<<<-]>>>++++++++++++++.>++++.-------.+++++++++++++.---.<<++.>>++++++++++++++.----------.++++++.<<.>>---------------.+++++++++.+++.<<.>>.-------------.----.+++.+++++.+++++.-------.<<.+.<++++++++++.
```
