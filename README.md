# CompSci-251-Programming-Assignment-7-solution

Download Here: [CompSci 251 Programming Assignment 7 solution](https://jarviscodinghub.com/assignment/compsci-251-programming-assignment-7-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

In this assignment, you will be creating a majorly enhanced version of the Tic-Tac-Toe game from the
Dean & Dean textbook (see Chapter 18.7, p. 830). This starter code is also available on D2L.
2 Requirements
You may use the code in the book as a template, but it will require many large changes. In particular, your
game must add the following features/properties.
Marking a Cell The template just sets the text of a button to either X or O. Instead, we will be setting
the icon of a button to be either an image of an X or an O. This will require a few change to the template
(notably, checking if a cell has already been selected). Assuming there is a file called x.png in the same
directory as the Java file, the following code will read an image from disk:
ImageIcon icon;
try {
icon = new ImageIcon(ImageIO.read(getClass().getResource(“x.png”)));
} catch (IOException ex) {
// …
}
You can set an icon image of a button with its setIcon method. You can remove an image from a button
by setting the icon to null.
Terminating Conditions After a new cell is marked by a player you must check to see if the game has
finished. A player has won the game if they have marked three cells in a row (in total, there are eight ways
for a player to win a game). You must exhaustively check each line on the board to see if all three buttons
have the same icon. The game is also over if it is a draw. A draw happens when no cells are left unmarked
but there is no winner. If a player wins a game, you should change the background color of the winning
buttons to blue. You can change the background color by using the setBackground method. You may also
need to add the following code into the main method (it should be the first thing you do).
try {
UIManager.setLookAndFeel(UIManager.getCrossPlatformLookAndFeelClassName());
} catch (Exception ex) {
e.printStackTrace();
}
1
Win Counters You must add three labels to the frame which track how many games were won by player
X, how many games were won by player O, and how many games were a draw. When a game terminates,
you must increase the correct counter (which should just be integer member variables) and update these
labels accordingly.
First Player Toggle Buttons You should add two radio buttons in a button group that will determine
if player X or player O gets to play first. These buttons should be disabled while a game is in progress (after
the new game button is pressed but before the termination condition), and enabled when a game terminates.
You should make a boolean member variable which will signify that player X goes first if the value of this
variable is true, and player O goes first if the value of this variable is false. You should add action listeners
to these buttons which will set this value appropriately.
New Game Button You should add a new game button. This button will clear images and background
color from all the buttons, disable the player toggle buttons, and will set the turn to be to the appropriate
player. No game is in progress when the frame is first created (before this button is pressed for the first
time). If this button is pressed during a game, you should start a new game but not change the win or draw
counts (it is a forfeit).
3 GUI
You must make the frame conform to the following screenshots as closely as possible. My solution used several
nested JPanel instances to get alignment to work properly. The outer-most panels uses BorderLayout and
the inner panels use GridLayout or FlowLayout (the default). It is up to you to try to emulate this screen.
4 Submission
Submit your entire eclipse project in a zip file to the D2L dropbox before the posted deadline.
