# Student Questions

## Lesson 1

Q: Using Git Bash on Windows, how do you change directories to the c drive?

A: <code> cd /c </code>
<hr>

Q: After using <code> git log </code>, I have pages and pages of information to scroll through. How do I get back to the prompt to enter a new command?

A: You can get back to the prompt by pressing <code> q </code> for 'quit'
<hr>
Q: Lessons 28-30 seem out of date, where can I find 2021 era instructions for upgrading the Git Bash prompt? 

A: <a href="https://github.com/ekn394/KPL-Intro-to-Git-and-GitHub/blob/main/upgrade-git-bash-prompt.md" target="_blank"> 2021 Instructions (for Windows)</a>
<hr>
Q: The videos show opening files in Sublime Text (version 2) from the command line, but their instructions don't work for me? What should I do?  

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

<hr>

## Lesson 3

Q: In number #3 ("Examining the New Repository") the instruction videos, and the quiz has the output saying 'Initial commit'. But that is not what I see when I follow the instructions to the letter. 

A: It looks like since those video lessons were produced, Git has been updated to replace that "Initial commit" message with "No commits yet".  I think this is related to the previous quiz quesion about how a new git repository has zero commits. It might look confusing to see the words "Initial commit" when there have been none.  It is more intuative for it it to say "No commits yet" since the number of commits so far is zero.  The wording in the software is more clear, but the quiz question in #3 is asking you to put in what the message *used* to be, "Initial commit".   


Q: In #5 ("Staging Area"), similar to above, the git status output is from a previous version. 

A: Before you put files in the staging area, git status on your reflections folder might look something like this.

![image](https://user-images.githubusercontent.com/12129459/132280687-ed48d2da-e6f3-4bb8-beb8-fb78d599b9aa.png)
 
Then after using 
<code> git add theFileName </code>  to add the files I want to the repository. 

![image](https://user-images.githubusercontent.com/12129459/132280846-02d7d0e4-c541-407b-a84e-b2843c42ff30.png)

 Then, if I run git status again, I should see that there are now 'staged' changes.  Changes that are ready to be committed. 

![image](https://user-images.githubusercontent.com/12129459/132280917-ec57a4a3-5f78-4720-ac48-b8779ef9d431.png)

<hr>
Q: #8 The easy way.  Just add <code>-m "And then the message" </code> to add your message to your git commit. 

![image](https://user-images.githubusercontent.com/12129459/132284849-c66a14fa-8242-4d96-9cb7-694bdef8751f.png)

<hr>

Q: #8 The long way.  You are told to try to use <code> git commit </code> which will launch SOME text editor to give us a place to write our commit message.  I find myself in a screen that looks like ...

![image](https://user-images.githubusercontent.com/12129459/132283005-33419a34-c70a-420f-bfb8-2e39cf454510.png)

Depending on how you installed git, the default text editor is probably "Vim" showed above. Having to use this text editor is not recommended for beginners, or intermediate users.

How the hell do you even get out of here you ask?  Well, it is an intuative as typing the following 5 part spell. 

You type these characters in order: 

<li> ESC (The excape key)</li>
<li> <code> : </code></li>
<li> <code> x </code></li>
<li><code> ! </code></li>
<li> Enter </li>  

There were no spaces in there either. 

Hit escape

:x!  

Then press Enter.  

See how easy Vim is to use?  Yeah it is a nigthmare.  Ok, if you REALLY insist on opening up a code editor just to write your commit messages you can set the default code editor to something more user friendly. 

![image](https://user-images.githubusercontent.com/12129459/132283814-90139e7e-9942-4534-ad9e-0627b72b1fa8.png)

If you have Visual Studio Code installed, you can change your default code editor to that by entering the following git command. <br>
<code>export GIT_EDITOR="code --wait --new-window" </code>

or if you prefer to use notepad, you can instead enter 

<code>export GIT_EDITOR="notepad"</code>


<hr>

![image](https://user-images.githubusercontent.com/12129459/132284002-14762709-a51e-4a69-b853-7533acda6e80.png)

Then if you type git commit (with changes that are ready to be commited) you will see your visual studio code open up, with the beginnings of a message. 

<hr>

![image](https://user-images.githubusercontent.com/12129459/132284122-974a83bc-edde-4db1-88d3-754bbd2167b0.png)

You just supply a message and save and quit. 

<hr>

![image](https://user-images.githubusercontent.com/12129459/132284197-163f164c-7052-44d6-8538-0d57bc224597.png)

When you quit that text editor, and go back to your Git Bash, you will see that the git commit has happend using your message. 

<hr>

