# ASCII SPREADSHEET 123

Background
==========
Your task is to build a spreadsheet from scratch in Java or C++. Please document your steps as you go as we may ask you to justify your implementation after you turned in your work. Do comment your code. Unit tests are not required but highly recommended. Please tell us how to compile and run your code upon submission. A tarball submission will suffice.


## Task 0
Print out to the screen a 4x3 spreadsheet with empty cells. Each cell should have exactly 5 spaces in it. The following is exactly what you should print out to the screen.
1. Adjacent cells in the same row are separated by a pipe character (|).
2. Columns are label by English Alphabet (A, B, C, etc.). Don't worry about running out of letters if you have to insert a lot more columns later.
3. Rows are label by integers starting from 1.
4. Keep in mind that you'll have to update a cell's value. Choose your data structure wisely.

       A     B     C     D
    *-----------------------*
    |     |     |     |     | 1
    *-----------------------*
    |     |     |     |     | 2
    *-----------------------*
    |     |     |     |     | 3
    *-----------------------*

## Task 1
Add a command prompt at the end of the spreadsheet that can read in user input. Once the user presses enter, your program should consume, parse, and execute the command. Then, print out the resulting spreadsheet again to stdout. For now, just make sure you can read in user's input.

       A     B     C     D
    *-----------------------*
    |     |     |     |     | 1
    *-----------------------*
    |     |     |     |     | 2
    *-----------------------*
    |     |     |     |     | 3
    *-----------------------*

    Your command?>

## Task 2
Add the capability of assigning a float value to any given cell. The command needs to take the following lisp-like format.
    (define A1 3.14)

Example:

       A     B     C     D
    *-----------------------*
    |     |     |     |     | 1
    *-----------------------*
    |     |     |     |     | 2
    *-----------------------*
    |     |     |     |     | 3
    *-----------------------*

    Your command?> (define A1 3.14)

[enter]

       A     B     C     D
    *-----------------------*
    | 3.14|     |     |     | 1
    *-----------------------*
    |     |     |     |     | 2
    *-----------------------*
    |     |     |     |     | 3
    *-----------------------*

    Your command?>

If the length of the float number is larger than the default 5 space cell width, truncate the number and make the last character to be '>' to denote truncated values.

Example:
       A     B     C     D
    *-----------------------*
    | 3.14|     |     |     | 1
    *-----------------------*
    |     |     |     |     | 2
    *-----------------------*
    |     |     |     |     | 3
    *-----------------------*

    Your command?> (define A1 3.1415926)

[enter]
       A     B     C     D
    *-----------------------*
    |3.14>|     |     |     | 1
    *-----------------------*
    |     |     |     |     | 2
    *-----------------------*
    |     |     |     |     | 3
    *-----------------------*

    Your command?>


Example
       A     B     C     D
    *-----------------------*
    |3.14>|     |     |     | 1
    *-----------------------*
    |     |     |     |     | 2
    *-----------------------*
    |     |     |     |     | 3
    *-----------------------*

    Your command?> (define A1 12345.123)

[enter]
       A     B     C     D
    *-----------------------*
    |1234>|     |     |     | 1
    *-----------------------*
    |     |     |     |     | 2
    *-----------------------*
    |     |     |     |     | 3
    *-----------------------*

    Your command?> (define A1 12345.123)

What potential erroneous input will you need to watch out for?

## Task 3
