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
Linked list is important to understand because it is often asked in job interviews. New programmers find it difficult to implement because of pointers. Once we master the fundamentals, problems like this can be easily solved.
<!--more--> 

### What is a Linked List?

A linked list is a data structure that has the attributes of an **array**, but better in some aspects. It is a set of nodes where each node contains a data and a pointer. It also has a dynamic size unlike an array that has a fixed size.

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

### How do we reverse a Linked List?
This is how to reverse a linked list iteratively. 
{{< highlight java >}}public class ReverseLinkedList(Node head) 
	Node curr = head;
	Node prev = null;
	Node nex = null;
	while (curr != null) {
		nex = curr.next;
		curr.next = prev;
		prev = curr;
		curr = nex;
	}
	return prev;
{{< /highlight >}}

The runtime of this code is 100% faster than all Java submissions in LeetCode. I personally like the iterative approach because it can clearly show the implemention of the pointers

Here's a great book tackling all of the data structures and algorithms I've studied so far, we call it [CLRS](https://www.amazon.com/Introduction-Algorithms-3rd-MIT-Press/dp/0262033844). 