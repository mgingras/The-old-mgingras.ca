---
layout: project
title: Shitsweeper
categories: coding
---

#####*A twist on the classic game, minesweeper, where the consequences for an incorrect selection are a bit more vile*

<p><strong>Built using:</strong>&nbsp;&nbsp;<span title="Java" class="pict-prog-java icon-2x"> </span>Java</p>



This application is a quick and dirty mock up of the age old game of minesweeper, with the incongruous twist
that an incorrect choice will land you in a pile of s#it.

<!-- abridge -->

This game was mocked up in two steps. Initially it was created to be played on the command line. Once the game
starts you are prompted to press Enter and shown the command to quit at any time. After pressing enter the
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
as '@'. If you win you may play another game and your score is aggregated. However, if at any point you land on a mine,
 the entire board is displayed, as well as your final score, and the game terminates.

See the [code...](https://github.com/mgingras/stinky-game-command-line)

During the second iteration of development of this application I switched out the view to make use of the Swing graphical 
library for Java to allow for a prettier UI.

Here is a screenshot of a fresh game. Once you press start a timer is started and there is a bonus for finishing
quickly.   

<a href="http://www.flickr.com/photos/97299680@N08/9011402100/" title="stinkyNewGame by martingingras, on Flickr"><img src="http://farm4.staticflickr.com/3704/9011402100_835bd6e96f_z.jpg" width="599" height="600" alt="stinkyNewGame"></a>   

This is a screenshot of a finished game. As you can see, once you found all of the un-mined spaces the game is
ended and the board is revealed and you are given the option to play again.



<a href="http://www.flickr.com/photos/97299680@N08/9011402022/" title="stinkyWonGame by martingingras, on Flickr"><img src="http://farm8.staticflickr.com/7343/9011402022_d06fafba00_z.jpg" width="603" height="596" alt="stinkyWonGame"></a>   


See the [code...](https://github.com/mgingras/stinky-game-swing)