TicTacNope
==========

The computer works as follows:
1.  Is the player about to win?
   a.	Yes: Move to stop the player and end turn
   b.	No: Check next loop
2.	Is the computer about to win
   a.	Yes: Move to win and end turn
   b.	No: Check next loop
3.	Did the player move to a corner?
   a.	Yes: Is the center already taken?
     i.	Yes: Perform failsafe and end turn
     ii.	No:  Move to the center and end turn
   b.	No: Check next loop
4.	Did the player move to the center?
   a.	Yes: Is the left corner already taken?
     i.	Yes: Move to next corner available corner and end turn
       1.	No available corner?
         a.	Yes: Perform the failsafe and end turn
         b.	No: Move to next loop
     ii.	No: Move to the left corner and end turn
   b.	No: Check next loop
5.	Did the player select an edge?
   a.	Yes: Is the top left corner already taken?
     i.	Yes: Move to next corner available corner and end turn
       1.	No available corner?
         a.	Yes: Perform the failsafe and end turn
         b.	No: Move to next loop
     ii.	No: Move to the left corner and end turn
   b.	No: Check next loop
6.	Computer failsafe
   a.	Check to see if to left space is free
    i.	Yes: Move there and end turn
    ii.	No: Repeat for next square
    
If the computer moves at the end of any of these loops, it sets the computer turn variable to zero and does not move until the player moves.
