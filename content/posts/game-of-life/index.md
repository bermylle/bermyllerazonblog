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

A cell automaton game made by John Conway. It is zero-player game where cells follow a specific set of rules. A simulation where a cell group may have the tendency to survive or die out immediately. 
<!--more--> 
{{< figure src="/game-of-life/gol.gif" class="full-wide-width" >}}

This is the first project given to us in CS 11 (Introduction to Computer Science). When the project's specification was uploaded on our facebook group, I started straight away because I wanted to learn. I had a mindset that I should do my projects as early as I can. 

Programming is my **passion** and I always had the urge to code even if I have a lot of other things to do. I love coding as much as I love pizza.

The less I know, the more I want to learn. There are a lot of things I need to practice and I'm not going to stop until I'm satistfied with my skillset.

I coded nonstop in my dorm and since it's my first project, I thought it was gonna be fun.. Until I was introduced to pointers and arrays.

### C Implementation 


I wrote this C program with 890 lines of code. This is easy to implement with **pointers** and it should lessen the length of code, but with the deadline fast approaching I used 2D arrays. The image below is the actual program I made. 

{{< figure src="/game-of-life/gol-actual.gif" caption="40x20 grid R-pentomino " class="wide-width" >}}

### Problems Encountered

I had a problem coding the *random* option in the menu because if a user chooses that option, all types of creatures present in the program will have to occupy the specified grid. Most of the creatures are spread out in the grid, but I had to code a handler that would avoid overlapping creatures.

### Learnings

A year and a half later, I browsed my code for this project and I saw that my decision making in terms of coding approach is quite different now. I consider my coding style in this project to be 75% brute force. I had numerous for loops inside while loops which can be reduced to something simpler if I were to recode it. 

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
