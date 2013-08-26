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

Based on the reading in the book, I would presume it not to be okay. As common knowledge, devices can fail and corruption can also occur,
which could affect you significantly if your local copy of the repo is only kept on a USB drive.

The Git book we read also had some other good points, such as how GitHub can be very useful for collaboration. If working with a team,
using an online storage that also utilizes Git, and has the several helpful features such as branching, merging, tracking, and many other features,
is really helpful to any Software Development. It also allows for the ability to perhaps one day declare it open source, and to have the community work
on it, but also allows there to be several copies of the code, that are not only up to date, but also online which is much more reliable than a USB drive
or local repository. This also removes the need to carry around the copy of the repo on a USB drive, and can be opened anywhere with an internet connection.

Keeping it on the M drive is somewhat more reliable than a USB or your local drive, but is not nearly as easy to access as a GitHub repository if you are not using a Miami Computer.
In order to get onto your M drive you would have to navigate the Miami website to find out where to access this online drive, and many times it is very slow to access and download these
files.

With that being said, the M drive is better than a USB in some aspects, but an online repository such as Github is definitely superior, and should be the preferred
way of versioning and saving code whenever possible. If one didn't want their code to be public, they could even pay a small monthly fee of $7 for 5 private repositories.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

If you forgot your USB and had no online repository, such as one you would have it you had GitHub, you would have to run all the way back to get your USB drive,
or restart from scratch on what you had, if anything.

If you were starting new anyways, or decide to start new, the smart thing would be to use GitHub as an online storage and also to compare work with the rest of your
homework friends. This would allow you to compare your answers, and even fork eachothers respositories and use modify them as your own. If it was a group project,
you could even use one single repository, and make changes as a team instead of having to try and organize code sending through email or USB's.

Then when you went home after working on your homework with friends, you could simply pull from the repo, and make changes from your home computer, making the whole
task of keeping track of where your project is stored, and getting that project later, much easier.

#### 3. Morin, Exercise 1.1 (p. 23)

//I want to do this Recursively, although I'm not sure how to any less "code" than this...

//Simple PseudoCode class example of reading a file, and printing in reverse order
class exampleOne{

main(){
	File file = new File(); // Create a file to use, assume it has all the input
	printStuff(the file data); //Call a method to print the lines
}

void printStuff(the file data){
	nextLine = (next line of the file data);
	printStuff(rest of the file data);
	
	print(nextLine);
}



Final Comments By Myself:
I had to do some code, although I tried to do as little as possible.
The best solution I could think of was to do it recursively, which requires something I 
couldn't quite figure out how to get just right. I hope what I have is acceptable.
- Garrett
}

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

[Your answer here]

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - A blob in Git basically stores all a files data, with no access to it's meta data or it's name. Blob is a contraction of Binary Large OBject.
2. tree - A tree in Git represents a single level of directory information. A tree contains identifiers of Blobs, path names, and also some of their meta deta, all in one location.
A tree also has the ability to recursively reference itself, and other trees.
3. commit - A commit, as an object as it relates to Git, is an object that contains meta data for each change introduced into the repository, including the authors information.
Each commit points to one tree object, that has a "snapshot" of the repository when that commit was made. All commits can be traced backwards to the previous commit, eventually leading
to the intial commit, or first commit of a repository.
4. repo - TODO
5. hash - TODO