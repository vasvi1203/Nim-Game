# Nim Game
Mini project for Artificial Intelligence course.

Execute the following command to run the game.
> python3 nim.py

## About Nim Game
Given a number of piles in which each pile contains some number of objects. In each turn, a player can choose only one pile and remove any number of objects (atleast one) from that pile. The player who takes the last object is the winner.

## Nim-Sum
The cumulative XOR value of the number of objects in each pile at any point of the game is called Nim-Sum at that point. The optimal strategy for each player is to make the Nim-Sum zero for his opponent in each of their turn.

## Algorithm
```
1. Initialise the game with default:
     mode = player vs player
     player 1 = 1, player 2 = 2
     winner = none
     GUI for the game
2. Load menu for selecting mode
3. Select mode to load another menu accordingly
4. For player vs AI mode:
    while winner not declared
      if current player is player 1
        remove valid amount  of an object from a valid  row
        print move    
      else
        initialize board balanced to False
        copy game board
        check if the copied game board is balanced
        if already balanced, remove 1 object from the first non-empty pile
        else
          for row in rows
            remove objects one by one from that row
            if board is balanced, change board balanced to True and break
            if row becomes 0, recopy the original board
            print move
       if winner declared, end game
       else change player and continue
5. For player vs player mode
    while winner not declared
      if current player is player 1
        remove valid amount  of an object from a valid  row
        print move
      else
        remove valid amount  of an object from a valid  row
        print move
      if winner declared, end game
      else change player and continue
```

## Still from the game
