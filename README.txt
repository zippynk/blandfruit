Blandfruit v0.0.2
By Nathan "zippynk" Krantz-Fire: https://github.com/zippynk/blandfruit

(c) Nathan Krantz-Fire. Some rights reserved.

This documentation is available under the Creative Commons Attribution-ShareAlike 4.0 International License. The interpreter for Blandfruit, which may or may not be included, has its own license and is not governed by the Creative Commons Attribution-ShareAlike 4.0 International License unless stated otherwise.
A copy of the Creative Commons Attribution-ShareAlike 4.0 International License can be found at the following link: https://creativecommons.org/licenses/by-sa/4.0/

Blandfruit is a work-in-progress esoteric programming language.

Requirements:
Python 3
(Python 2 may or may not work)

Installing:
$ sudo cp blandfruit /usr/bin/blandfruit
(Must be CD'd into blandfruit's directory)

Running a Program:
$ blandfruit [FILEPATH] [OPTIONS]
(If using Python 2, try: $ python /usr/bin/blandfruit [FILEPATH] [OPTIONS])

Debug Mode:
If the --debug flag is put after the filepath, blandfruit will connect to a server hosted locally on port 42002 (which must be running) and send the character (see below) of each command executed to that server.

Commands:
> Outputs the working space to the terminal.
< Takes one character of input and appends it to the working space.
v Appends the contents of the working space to the variable with the name of the first argument. Takes 1 argument, a string.
^ Appends the contents of the variable with the name of the first argument to the workign space. Takes 1 argument, a string.
* Clears the working space.
_ Clears the contents of the variable with the name of the first argument. Takes 1 argument, a string.
" Inserts the first argument into the working space. Takes 1 argument, a string.
# Converts the variable with the name of the first argument to an integer. Takes 1 argument, a string.
` Converts the variable with the name of the first argument to a string. Takes 1 argument, a string.
+ Adds one to the variable with the name of the first argument. Takes 1 argument, a string. Note that the variable must be in integer format.
- Subtracts one from the variable with the name of the first argument. Takes 1 argument, a string. Note that the variable must be in integer format.
@ Sends the interpreter's code-reading index forward the number of characters specified in the first argument. Takes 1 argument, a number. Note that the interpreter index will start from the location of the @ character and that the character that it arrives at will be executed.
x Sends the interpreter's code-reading index forward the number of characters specified in the second argument if the variable with the name of the first argument equals the working space, or the number of characters in the third argument if the first argument does not equal the working space. Takes 2 arguments, a string and 2 numbers. Note that the interpreter index will start from the location of the @ character and that the character that it arrives at will be executed.

Data Types:
String is the default data type. It is used in most cases.
Integer can be used, but only for addition and subtraction. Integers cannot be worked with in the working space, printed out, inputed.

Arguments:
Some commands take arguments. If a command takes arguments, insert each one right after the command, and right after one another, putting a . at the end of each argument.

Comments:
Although there is no official way to make a comment, one can achieve the effect with the expression below:
_#####.v#####.*" COMMENT GOES HERE .*^#####._#####.

Unexpected Characters:
Are ignored.
