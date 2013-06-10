---
layout: project
title: Stinky Game
categories: coding
---

#####A minesweeper-like application where the consequences for selecting an incorrect tile are a bit more vile.

<p><strong>Built using:</strong>&nbsp;&nbsp;<span class="pict-prog-java icon-2x"> </span>Java</p>



This application is a quick and dirty mock up of the age old game of minesweeper, with the incongruous twist
that an incorrect choice will land you in a pile of s#it.
<!-- abridge -->

This game was mocked up in two steps. Initially it was created to be played in the command line. Once the game
starts you are prompted to press Enter and given the command to quit at any time. After pressing enter the
following "board" is displayed:


<pre style="width:60%;">
Score: 0
0 |**********
1 |**********
2 |**********
3 |**********
4 |**********
5 |**********
6 |**********
7 |**********
8 |**********
9 |**********
  +----------
   0123456789

Enter &lt;Row#&gt;, &lt;Col#&gt; of piece to uncover: 
  
</pre>

The console then accepts entries in the form of "int,int", any other entry will be rejected and the user will be
re-prompted for an appropriate entry.

The game progresses with the same logic as traditional minesweeper, where the unknown spaces are represented with
'\*' , the known spaces have an integer number displaying the number of adjacent mines, and the miens are represented
as '@'. If at any point you land on a mine, the entire board is displayed, as well as your final score, and the
game terminates.

See the [code](https://github.com/mgingras/stinky-game-command-line)