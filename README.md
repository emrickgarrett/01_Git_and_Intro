Author
==========
Andy Shear, shearar
01_Git_and_Intro
================

Practice with basic git functions, and intro to study of Data Structures

Reading
=======

**Version Control with Git, 2nd Ed**. Loeliger and McCullough. 

http://proquest.safaribooksonline.com/book/databases/content-management-systems/9781449345037/version-control-with-git/id302681?uicode=ohlink (Free access through www.lib.miamioh.edu, but limited to 100 simultaneous users across all OhioLink. I recommend downloading/printing the required readings ahead of time, just in case.)

Read only the following:

1. Chapter 1
  * Background
  * The Birth of Git
2. Chapter 3: Getting Started
  * Intro
  * The Git Command Line
  * Quick Introduction to Using Git (read all sections)
  * Configuration files (Intro only, may skip part on aliases)
3. Chapter 4: Basic Git Concepts
  * Basic concepts (read all)
  * Object store pictures
  * Git concepts at work (read all)
4. Chapter 21: Git and Github

**Open Data Structures in C++**. Morin. 

http://opendatastructures.org/ (Free access. I recommend downloading the PDF version.)

Read the following:

1. Chapter 1 (pp. 1-20)

Homework
========

1. Create an account with github.com. You may select the free account. If you want to get some free private repos, you may apply at https://github.com/edu
2. Go to https://github.com/MiamiOH-CSE274/01_Git_and_Intro and fork the repo, which will create a copy of it in your github account.
3. Install git on your computer, if you do not already have it. I recommend installing http://windows.github.com/ if you use windows, or http://mac.github.com/ if you use Mac. HOWEVER, I highly recommend using the command-line tools for everything, and ignoring the GUI. I will not be providing help with configuring/using the GUI.
4. Clone your repo from github to your computer. When you are at the web page for your repo, `https://github.com/[your github id]/01_Git_and_Intro`, you will see info about how to clone it. The easiest way is to go to the command line terminal, and type `git clone git@github.com:[your github id]/01_Git_and_Intro.git`
5. Checkout your personal branch from the repo. Each student has a branch labeled by their Miami uniqueid. `git checkout uniqueid` ... for example, I would do `git checkout brinkmwj`
6. Complete the exercises below by modifying this file.
7. After you complete each answer, be sure to create a new commit with the changes (using `git add README.md` and `git commit -m` as appropriate). Also, be sure to upload to github frequently by using `git push`
8. If I don't see at least 4-5 commits on this homework, I'm going to be unhappy.
9. Once complete, send me a pull request. You should send from your branch in your github repo, to your branch in the MiamiOH-CSE274 repo. This is your official "turn in" of the homework, which I will grade.
10. Double check that you did the right thing by going to https://github.com/MiamiOH-CSE274/01_Git_and_Intro/pulls and making sure that your pull request is there, and looks like you expect. Optimism is the root of all evil.

Exercises
=========

#### 1. Based on the reading in the Git book, is it okay to keep your local copy of your repo on a USB drive and just carry it around? Explain why or why not. What about keeping it on the M: drive?

It is not okay to keep another copy of a repo, whether its on a USB drive or on the M drive. There is a risk of losing or damaging a USB drive, resulting in the loss of un-synced data. Keeping it on the M drive is also unsafe, as GIT does not transfer configuration settings from computer to computer; so what works on one machine may not work on the other.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

You should clone your repo to a computer in the lab, then commit your work back to GIT when you are done. This way, you can save your work, and revert to a previous version that was in sync with your local repo if anything goes wrong.

#### 3. Morin, Exercise 1.1 (p. 23)

1. Read in each line as a string, and store each string as an object in a stack type array the size of the input files number of lines. Since a stack is a LIFO data structure, the last item added can be printed, then popped off the stack.  Since pop removes the most recent item added to the stack, this process of print/pop can be repeated until the first element of the array is printed and removed.  This will have printed every line in reverse order.

2. Read in each line as a string, and store each string as an object in a stack type array of size 50.  Do this until 50 lines are stored or there are no more lines to read.  Print the most recently added item at the tail of the array, then pop the item from the array.  Repeat this until the item at the head of the array is popped, thus printing 50 (or less) lines in reverse.  Repeat this entire process until the last set of lines are read into the array, at that point the final set of lines will be printed in reverse, and the repeat cycle will terminate.

3. Read in each line as a string, and store each string as an object in a queue type circular array of size 43.  Once the array is filled, check if the string at the tail of the queue is empty, if so, print the item at the head of the queue.  Remove the item at the head of the queue, and read in the next line to the tail of the queue.  Since this is a circular array, just incriment and perform a modulous operation on the head and tail pointers each time a new line is added.  The modulous operation will keep the head and tail pointers in bounds and make the array circular.  Repeat this process until there are no more lines to read.

4. Read in each line as a string, and store each string as an object in a USet type linked list.  Set the first line of input to the head of the linked list using the add(x) method, and print this line (since it is unique).  For each subsequent line read in, use the add(x) method to add it to the list.  The add(x) method uses the find(x) method to ensure there are no duplicate lines in the list.  Add(x) returns true if it is added as a unique line, and false if it is a duplicate.  Print the particular line if add(x) returns true.  Repeat until there are no more lines to read in.  This ensures only necessary memory is used as the linked list will expand as items are added, and only non-duplicates will be added.

5. Read in each line as a string, and store each string as an object in a USet type linked list.  Set the first line of input to the head of the linked list using the add(x) method.  For each subsequent line read in, use the add(x) method to add it to the list.  The add(x) method uses the find(x) method to ensure there are no duplicate lines in the list.  Add(x) returns true if it is added as a unique line, and false if it is a duplicate.  Print the particular line if add(x) returns false.  Repeat until there are no more lines to read in.  This ensures only necessary memory is used as the linked list will expand as items are added.  The linked list will hold the first occurance of each line, any duplicates will be printed.

6. Read in each line as a string, and store each string as an object in a SSet type doubly linked list.  Set the first line of input to the head of the linked list using the add(x) method.  For each subsequent line read in, use the add(x) method to add it to the list.  The add(x) method uses the find(x) method to ensure there are no duplicate lines in the list.  In this SSet, the find(x) method also returns the location of a value y such that the size of string y >= the size of string x.  The add(x) method will then add the new line to the doubly linked list before the location find(x) returned, or at the tail if find(x) determines it to be a unique line but returns null (meaning it is the longest line yet).  The doubly linked list can expand in either direction, allowing items to be added anywhere, so the list will be sorted as it is created.  Repeat until there are no more lines to read in, then print the doubly linked list by looping from head to tail.

7. Read in each line as a string, and store each string as an object in a SSet type doubly linked list.  Set the first line of input to the head of the linked list using the add(x) method.  For each subsequent line read in, use the add(x) method to add it to the list.  The add(x) method uses the find(x) method to return the location of a value y such that the size of string y >= the size of string x.  The add(x) method will then add the new line to the doubly linked list before the location find(x) returned, or at the tail if find(x) returns null (meaning it is the longest line yet).  The doubly linked list can expand in either direction, allowing items to be added anywhere, so the list will be sorted as it is created.  Repeat until there are no more lines to read in, then print the doubly linked list by looping from head to tail.  Since the find(x) method no longer searches the list for duplicates, all lines will be printed in order, including all duplicate lines.

8. Read in each line as a string, and store each string as an object in an array the size of the input files number of lines.  Using a for loop starting at x=0, print the corresponding string at that position in the array, then incriment the loop by 2, until x > the size of the array.  Then using another for loop starting at x=1, print the corresponding string at that position in the array, then incriment the loop by 2, until x > the size of the array.  This will print the even numbered lines, and then the odd numbered lines in order.

9. Create and array the size of the input files number of lines.  Read in each line as a string, and store the string as a pair along with a boolean value of false.  Then, store each pair in the array in acending order.  Inside a for loop, use a random() function to create a random integer between 1-100, and % the size of the array.  Use this number to check if that spot in the array has a pair with a boolean value false, if so, print the string and change the value to true.  If the value is true, incriment the array index by one and check again.  If the end of the array is reached, recall the origional array index, and decrement the array index by one until a space is found.  The for loop will end once it repeats "size of the array" times.  At this time, all pairs will have been added to the array in random order and will include a true boolean value, ensuring no duplicates were added.  Using another loop, iterate through the array and print the string in each pair.  This will print all lines in a random order.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

Exercise 1.4


