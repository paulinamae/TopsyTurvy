# TopsyTurvy
Connect-Four style game programmed entirely in C! Two players, BLACK and WHITE, each take turns making moves on a game grid. Each player can either:
  * drop their designated piece in a column, using either single-digit or letter identifiers for columns OR:
  * **offset**, which removes the current player's oldest piece and the opponent's newest piece on the board
  * **disarray**, which flips the entire board over the horizontal axis, adjusting for gravity
A player wins when the desired run length is reached.

Makefile is configured to support **play.c**, the main executable. To play, run:

**make play**
**./play -h # -w # -r # (-m/-b)**

* "-h #" refers to the desired height of the game board
* "-w #" refers to the desired width of the game board
* "-r #" refers to the **run length** of the game, which is the number of pieces needed in a row to win
* "-m/-b" refers to the choice between "-m" or "-b", which determines the usage of either a matrix or a bit representation of the board
  * ^^While this choice is arbitrary in terms of gameplay, the bit representation uses significantly less memory, while the matrix representation allows for a faster **disarray** move using     multithreading
  * Please only choose one of the two options

Replace all "#" characters with integers.
