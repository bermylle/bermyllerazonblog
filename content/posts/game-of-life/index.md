---
title: Game of Life
subtitle: # Optional, will be displayed bellow the title of the page; remove this line to generate an automatic subtitle
date: 2020-05-12
categories:
  - Game
  - C
banner:
  #src: g.jpg # Optional, the filename of the banner, by default banner.jpg
  caption: # Optional, the caption of the banner
  href: # Optional, a link on the caption
draft: false


---

A cell automaton game made by John Conway in which a group of creatures may tend to survive or die out immediately. It is a zero-player game where cells follow a specific set of rules. 
<!--more--> 
{{< figure src="/game-of-life/gol.gif" class="full-wide-width" >}}

This is the first project given to us in CS 11 (Introduction to Computer Science). When the project's specification was uploaded on our Facebook group, I started doing it straight away. I have a mindset that I should do my projects as early as I can. 

I believe that the less I know, the more I want to learn. There are a lot of things I need to practice and master in this tech field. I'm not going to stop until I'm satisfied with my skillset.

I coded nonstop in my dorm since it's my first project. I thought it was gonna be fun.. Until I was introduced to pointers and arrays.

### C Implementation 

I wrote this program with 890 lines of code. I realize now that it can be easily implemented with **pointers** which will reduce the lines, but with the deadline fast approaching I used 2D arrays. The image below is the actual program I made. 

{{< figure src="/game-of-life/gol-actual.gif" caption="40x20 grid R-pentomino " class="wide-width" >}}

### Problems Encountered

I had problem coding the *random* option in the menu because if a user chooses that option, all types of creatures must be present in the specified grid. Most of the creatures are randomized out in the grid, but I had to code a handler that would avoid overlapping creatures.

### Learnings

When I browsed my code for this project, I saw that my decision making in terms of coding approach is quite different now. I coded this project with brute force style. I am very grateful for this experience because I had a lot of fun doing it. 

#### Sample code from my project *yikes*
{{< highlight C >}}
void calculate(arrayTable tableA, int grid) {
	arrayTable tableB;
	int height, width;
	if (grid == 1){
	for (height = 0; height < HEIGHT; height++) {
		for (width = 0; width < WIDTH; width++) {
			neighbor = countNeighbor(tableA, height, width, grid);
			if (neighbor==3) {
				tableB[height][width] = ALIVE;
			} else if (neighbor == 2 && tableA[height][width] == ALIVE) {
				tableB[height][width] = ALIVE;
			} else {
				tableB[height][width] = DEAD;
{{< /highlight >}}

This is the function I used to determine whether the neighboring cells are alive or dead. 

You can visit my [Github](https://github.com/bermylle) to see the source code for this project.