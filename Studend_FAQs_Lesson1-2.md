# Student Questions

## Lesson 1

Q: Using Git Bash on Windows, how do you change directories to the c drive?

A: <code> cd /c </code>
<hr>

Q: After using <code> git log </code>, I have pages and pages of information to scroll through. How do I get back to the prompt to enter a new command?

A: You can get back to the prompt by pressing <code> q </code> for 'quit'
<hr>
Q: Lessons 28-30 seem out of date. Where can I find 2021 era instructions for upgrading the Git Bash prompt? 

A: <a href="https://github.com/ekn394/KPL-Intro-to-Git-and-GitHub/blob/main/upgrade-git-bash-prompt.md" target="_blank"> 2021 Instructions (for Windows)</a>
<hr>
Q: The videos show opening files in Sublime Text (version 2) from the command line, but their instructions don't work for me. What should I do?  

A: Don't stress out about which code editor you use. Sublime Text, Atom, Visual Studio Code, Notepad++, or just plain Notepad. 
If you wanted to be able to launch a good coding text editor from Git Bash, I recommend downloading and installing <a href="https://code.visualstudio.com/" target="_blank"> Visual Studio Code</a>. 
<p>Then, you can use the word <code> code </code> and then the name of the file you want to open. This will launch Visual Studio Code with that file open. 

![image](https://user-images.githubusercontent.com/12129459/131731162-9b1be166-72cf-4d64-a1e4-7a7e3410f61a.png)
<hr>

## Lesson 2

Q: "Working on #11 ("Finding a bug"), but I can't play the game by clicking on the 'Play the Game Here' link."

A: In #10 ("Cloning a New Repository"), you had to use <code>git clone</code> to download a copy of the game's git repository.

![image](https://user-images.githubusercontent.com/12129459/131723143-3a9ec536-1319-4321-a11a-48ff329f04a8.png)
<br>
Then, if you navigate to that freshly downloaded folder, there is a file in there (index.htm) that will launch the game in your webbrowser. 
<br>
![image](https://user-images.githubusercontent.com/12129459/131723227-7757eb33-f6eb-40da-a75f-f73279e4a0ea.png)

or... from Git Bash, you could type 

<code>start index.htm</code>

<hr>

Q:  I only see the most recent 4 commits on my screen.  

A: The scroll wheel on your mouse can be deceiving when using unix era software like our Git Bash command line.  Scrolling down with the mouse wheel shows that you are at the bottom of the Git Bash window.  But Git Bash is currently in a different 'mode' where it is trying its best to show you a lot of output text.  In this mode the controls have changed to allow you to scroll through it with the keyboard.  In this mode, the up and down arrow keys will scroll up and down by one line at a time.  Note that under normal circumstances, the 'up' key shows you your most recent command, but here, the up key scrolls up through the text by one line.  To go up or down by entire pages you can use the PAGE DOWN or PAGE UP keys on your keyboard.  
**To exit this mode, press <code>q</code>**

<hr>

Q:  On question 12, although we can use git diff to find WHERE the bug occurs, we are asked to determine exactly WHAT is wrong with the code. 

![image](https://user-images.githubusercontent.com/12129459/132396507-748a1f4d-9177-4385-8a9e-2b7a379af4a5.png)


A:  This one could be tricky for sure.  In a lot of common programming languages (C, Java, JavaScript) the concept of 'or' is written with two vertical bars like this <code>||</code>.  But if you didn't know that bit of trivia, you could still guess that the correct answer was the one that created 'several "if" statements'.  

![image](https://user-images.githubusercontent.com/12129459/132396677-73771e1d-c0ac-4732-b6f6-50725bd8b3ee.png)

Don't worry if you didn't get that one though. Being able to read JavaScript wasn't/isn't a prerequisite for this Git focused course.  
