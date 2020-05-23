---
title: Understanding Linked Lists
subtitle:
date: 2020-05-23
weight: 
categories:
  - Learning
  - Linked List
banner:
  #src: g.jpg # Optional, the filename of the banner, by default banner.jpg
  caption: # Optional, the caption of the banner
  href: # Optional, a link on the caption
draft: false


---
Can you reverse a linked list? If you can code it or understand the concept of it, then you are in the path of being a great developer.
<!--more--> 
Here's a great book tackling all of the data structures and algorithms I've studied so far, we call it [CLRS](https://www.amazon.com/Introduction-Algorithms-3rd-MIT-Press/dp/0262033844). 

### What is a Linked List?

A linked list is a data structure that has the attributes of an **array**, but better. It is a set of nodes where each node contains a dataue and a pointer. It also has a dynamic size unlike an array that has a fixed size.

The image below is an example node of a **singly linked list**.
{{< figure src="/linked-lists/linked.png">}}

A *singly linked list* has a **pointer** to the next node and a **key** part that stores the data.

### Java Representation of a Singly/Simple Linked List

{{< highlight java >}}public class Node 
	int data;
	Node next;
	Node(int data) {
		this.data = data;
	}
	Node(int data, Node next) {
		this.data = data;
		this.next = next;
	}
{{< /highlight >}}