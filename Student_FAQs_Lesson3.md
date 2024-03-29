# Student Questions

## Lesson 3

### General Suggestion 

You can open up a Git Bash style Terminal from <em>within</em> Visual Studio Code.  That way you don't have to keep switching between your Git Bash program where you type your git commands and a code editor where you make your edits.  You can do both from the same spot!  This is totally optional, and never mentioned in the course, but I find it handy.

To try this, first open Visual Studio Code. 

![image](https://user-images.githubusercontent.com/12129459/133833512-6bab910a-922b-4091-9698-bf9e732b6e6b.png)

On the top menu bar, there should be a drop down menu called "Terminal".  Select the first option which should be "New Terminal"
  <hr>

  
![image](https://user-images.githubusercontent.com/12129459/133833020-a0270253-008b-4515-a008-b911c9eba453.png)

  This will create a new section at the bottom of your screen that you can use for "command line" tasks.  

  The downside is that by default it will open in "powershell" mode which we don't want.  
  
  <hr>
  
![image](https://user-images.githubusercontent.com/12129459/133833295-8b3c3a40-e09e-42d7-bdae-ca0c9535275d.png)

  Click the down arrow to select a new <em>type</em> of terminal.  We want to select Git Bash since that is what we are familiar with at this point. 

<hr>

![image](https://user-images.githubusercontent.com/12129459/133833594-d7524595-a559-4b88-8d7b-1472c019770f.png)

You can now do all of your git commands here if you want.  The only difference I have noticed so far is that the Git Bash simulator within Visual Studio gives you the ability to use CTRL-C to copy and CTRL-V to paste (neither of those keyboard shortcuts were available on the more formal "Git Bash" software we had been using up to this point). 

<hr>

### #3

Q: In number #3 ("Examining the New Repository") the instruction videos, and the quiz has the output saying 'Initial commit'. But that is not what I see when I follow the instructions to the letter. 

A: It looks like since those video lessons were produced, Git has been updated to replace that "Initial commit" message with "No commits yet".  I think this is related to the previous quiz quesion from Lesson 2, about how a new git repository has zero commits. It might look confusing to see the words "Initial commit" when there have been none.  It is more intuative for it it to say "No commits yet" since the number of commits so far is zero.  I think that the present day wording "No commits yet" is more clear, but the quiz question in #3 is asking you to put in what the message *used* to be, which was "Initial commit" at the time when these videos were created.    

<hr>

### #5
Q: In #5 ("Staging Area"), similar to above, the git status output is different from the previous version that is used in the videos. 

A: Before you put files in the staging area, if you run the <code>git status</code> comand in your reflections folder, you might look something like this.

![image](https://user-images.githubusercontent.com/12129459/132280687-ed48d2da-e6f3-4bb8-beb8-fb78d599b9aa.png)
 
Then you can use <code> git add theFileName </code>  to add the files to the repository. 

![image](https://user-images.githubusercontent.com/12129459/132280846-02d7d0e4-c541-407b-a84e-b2843c42ff30.png)

 Then, if you run <code> git status </code> again, you should see that there are now 'staged' changes.  These are changes that are ready to be committed. 

![image](https://user-images.githubusercontent.com/12129459/132280917-ec57a4a3-5f78-4720-ac48-b8779ef9d431.png)

<hr>

### #8 The easy way. 

Just add <code>-m "And then the message" </code> to add your message to your git commit. 

![image](https://user-images.githubusercontent.com/12129459/132284849-c66a14fa-8242-4d96-9cb7-694bdef8751f.png)

<hr>

### #8 The long way.

You are told to try to use <code>git commit</code> which will launch SOME text editor to give us a place to write our commit message.  I find myself in a screen that looks like ...

![image](https://user-images.githubusercontent.com/12129459/132283005-33419a34-c70a-420f-bfb8-2e39cf454510.png)

Depending on how you installed git, the default text editor is probably "Vim" showed above. Having to use this text editor is not recommended for beginners, or intermediate users.

How do you even get out of this Vim program you ask?  Well, it is as intuative as typing the following 5 instructions in a row. 

You type these characters in order: 

<li> ESC (The escape key)</li>
<li> <code> : </code></li>
<li> <code> x </code></li>
<li><code> ! </code></li>
<li> Enter </li>  

There were no spaces in there either and you get no visual feedback until you are finished, so you don't know if it is working or not until you press Enter and hope for the best. To summarize those instructions again a different way,

Hit escape

<code>:x!</code>  

Then press Enter.  

See how easy Vim is to use?  Yeah, it is a nigthmare.  Ok, if you wanted to open up a code editor to write your commit messages, you can set the default code editor to something more user friendly. 

![image](https://user-images.githubusercontent.com/12129459/132283814-90139e7e-9942-4534-ad9e-0627b72b1fa8.png)

If you have Visual Studio Code installed, you can change your default code editor to that by entering the following git command: <br>
**updated Sept 23, 2021 to the method that sets the default editor and now REMEMBERS that choice in the future. 

<code>git config --global core.editor "code --wait"</code>

or ...

<code>git config --global core.editor "notepad"</code>
...if you prefer to use notepad. 

<hr>

![image](https://user-images.githubusercontent.com/12129459/132284002-14762709-a51e-4a69-b853-7533acda6e80.png)

Then if you type <code>git commit</code> (with changes that are ready to be commited) you will see your chosen code editor open up to your commit message (in this example the code editor is Visual Studio Code). 

<hr>

![image](https://user-images.githubusercontent.com/12129459/132284122-974a83bc-edde-4db1-88d3-754bbd2167b0.png)

You just supply a message and save and quit. 

<hr>

![image](https://user-images.githubusercontent.com/12129459/132284197-163f164c-7052-44d6-8538-0d57bc224597.png)

When you quit that text editor, and go back to your Git Bash, you will see that the git commit has occurred using your message. 

<hr>


### user.name and user.email 

At some point in this lesson you MAY run into a problem where Git needs a user.name and user.email to put a name to whoever is writing git commits.  It may detect that the way you logged in to your computer happens to have a default name and email and attached to it, and it may decide to use that. But it may have trouble during a commmit and ask for a user.name and user.email to attribute the changes being made to a person.  

To set this up once so you never need to do it again.  

<code>git config --global user.name "Evan Nordquist"</code>

and then 

<code>git config --global user.email "evan.nordquist@kpl.org"</code>


If you wanted to make name and email credentials that were specific to the git repository you are working on, then leave out the <code>--global</code>

<hr>

### #11 

#11 - It isn't explicitly mentioned on this page, but you are supposed to cd your way to the asteroids folder for this question. 

To open game.js in notepad you could type 

<code>notepad game.js</code>

or to open it in Visual Studio Code (if you have it installed) 

<code>code game.js</code>

<hr>

### #17

#17 - Just to start off with a slightly easier example, I want to see the branch diagram for what the asteroids folder looks like at the START of question 17. 

![image](https://user-images.githubusercontent.com/12129459/132524540-7459a5e7-3397-4727-829b-84d997186fd4.png)

I am asking for <code>git log</code> in <code>--graph</code> mode, and using <code>--oneline</code> makes each git commit show up as one line. 

Where we started with this repo when we used <code>git clone</code> to get it, shows up as commit id 3884eab (origin/master, origin/HEAD) Add color.

Then after that we added a new commit (9af40cc in my case) to the main branch which fixed the bullet delay bug.  

Then we made a new branch called easy-mode and have one commit there where we make the asteroids break into 2 peices instead of 3. 

It asks you to draw a diagram with pen and paper what is going on in the recent commits.  Here is my drawing BEFORE including the new coins branch.  

![image](https://user-images.githubusercontent.com/12129459/132526700-af5c8b70-b9e3-4e1e-8f98-4838b9c8c249.png)

<hr>

### #17 Continued.  

Trying to get the history including the coins branch, gives you an error...

![image](https://user-images.githubusercontent.com/12129459/132527786-3487f6c2-c41b-478e-ba5f-fdf2071fdb46.png)

... if you don't FIRST checkout the coins branch.  

<code>git checkout coins</code>

![image](https://user-images.githubusercontent.com/12129459/132529554-eef186b2-51e6-4fec-a064-fb06a2ca24ac.png)

A new diagram for this might look like the following.  Where in the past the coins branch split off the master branch and made 4 commits.  

![image](https://user-images.githubusercontent.com/12129459/132529409-22747593-c80e-4aee-934e-91ea2d3b1a36.png)

<hr>

### #24

24 Merging on the Command Line

Use <code> git branch </code> to SEE which branches of Asteroids you can see.  YOU MIGHT see something like this.  

![image](https://user-images.githubusercontent.com/12129459/132578005-d572dfd3-c77f-4ac1-b219-12115d74b90d.png)

If you DON'T see coins in that list, use <code>git checkout coins</code>  from within the asteroids folder.  That should put you on the coins branch.  (Which we don't want, but this is how you enable your Git Bash to be able to see it).  

Do you see that asterisk beside one of the branches?  That indicates which one you have 'checked out', that is the one that will be updated when you make commits.  

<hr>

We want to update the master branch, so we want to checkout the master branch.  

<code>git checkout master</code>

![image](https://user-images.githubusercontent.com/12129459/132578334-a5c7e905-aa16-44d7-aa70-07400121588a.png)

<hr>

You can double check that you are ON the master branch (it should have an asterisk, and you should also see the 'coins' branch listed now when you type <code>git branch </code>

![image](https://user-images.githubusercontent.com/12129459/132578501-c0088f8b-045c-42a7-82f8-d04f3f203327.png)

<hr>

### Side track: Do you have a code editor setup for your Git Bash (covered in #8 but repeating here)

When we merge the two branches together we will be asked to make a commit message, so before we do that, this is probably a good time to make sure that your git program will open a text editor that you are comfortable with.  

If you have Visual Studio Code installed, you can change your default code editor to that by entering the following git command: <br>
<code>export GIT_EDITOR="code --wait --new-window" </code>





or if you prefer to use notepad, you can instead enter: 

<code>export GIT_EDITOR="notepad"</code>


**Update Sept 23, 2021** Those above solutions work for THAT particular session while you are using Git Bash.  But if you wanted to make those changes more permanent, you could instead type...

<code>git config --global core.editor "code --wait"</code>
To use Visual Studio Code more permanently.  (Yes, you can always switch it to something else if you change your mind) 

or 

<code>git config --global core.editor "notepad"</code>
To use Notepad permanently. 


<hr>

### Back to #24
If you are ready to merge the two branches together ... 

<code>git merge master coins</code>

![image](https://user-images.githubusercontent.com/12129459/132579471-14df643e-194f-470c-85e6-641c50457c74.png)


### #24 Optional - Make the Coins Yellow, extra credit assigment. 

First look through the <code>git log</code> to look for a clue about where to even start.  I do remember there being a commit message called "Add color" so that sounds like a good place to start.  Use <code>git log</code> to find the commit with the message 'Add color'.  Although it was referring to the ship and asteroids, it will tell us how things are given colour in this game which will be helpful.

![image](https://user-images.githubusercontent.com/12129459/132584480-0d4d9ef1-ec56-4fc0-8932-053ba5868c5e.png)

Ok, so commit 3884ea adds color to the game.  

To see what was added in that commit, we can use <code>git show 3884ea</code> to 'show' the differences between that commit and it's parent.  Which commit *is* the parent of this commit is less clear now, since we have merged two branches together.  At this point <code>git show</code> will give us the information that we need. 

![image](https://user-images.githubusercontent.com/12129459/132585104-b9b3a2ad-ab31-4b28-b5d9-916f9a872847.png)

There is a line of code that looks like  **Ship = function()**... and just below that there are the properties: <br>
<code>this.color = 'navy'</code><br>
<code>this.solid = true;</code><br>

And a little later there is a line that looks like **Asteroid = function()**... with the properties: <br>
<code>this.color = 'lightgrey'</code><br>
<code>this.solid = true;</code><br>

So... in our most recent copy of that file *game.js* we should probably look for something called **Coins = function()***... and then add the properties:<br>
<code>this.color = 'yellow'</code><br>
<code>this.solid = true;</code><br>

<hr>

That's the game plan anyways, next let's open up game.js and see if we can find something that looks like Coins = function(). <br>

<code>code game.js</code><br>

Searching for the word coin (CTRL-F to search), I see that there is a line that contains ***Coin = function()*** and I will add the appropriate lines below that. 

![image](https://user-images.githubusercontent.com/12129459/132585912-f2ec6791-9570-4999-bdc3-bd075b6321d9.png)

*I found that orange is much easier to see than yellow*.

### #29 Resolving Merge Conflicts

After checking out the easy-mode branch,  <code>git checkout easy-mode</code>, we are then trying to merge in the master branch.  For clarification, we are trying to bring the updates on the master branch (coins that are now colored yellow) into the easy-mode branch (where astroids break into fewer peices).  **We are updating the easy-mode branch to have yellow coins, we are NOT updating the master branch be easier (asteroids that break in half)**.<br>

<code>git merge master easy-mode</code><br>
This does give me a merge conflict error (just as the video predicts). <br>
Q: How do I get to the place where it outlines the problems?<br>

A: When you got the merge error, it said that the problem came from the file called *game.js* <hr>

![image](https://user-images.githubusercontent.com/12129459/132721263-9c2a84ab-0f55-4077-9e06-7b55851c231e.png)

So you will want to open up that file.<br>

<code>code game.js</code><br>

It will now have the problem marked off with a series of <<<<<<<<  and >>>>>>>>>> markers

![image](https://user-images.githubusercontent.com/12129459/132721477-e24e04b5-ea53-4c35-b0b6-4384927f4c1a.png)

![image](https://user-images.githubusercontent.com/12129459/132722522-3a2eb409-700a-4e8a-8a02-f6d6665b0473.png)

<hr>

Delete the parts you don't want to keep (including the >>>>> and <<<<< and ||||||| lines.  

I want to keep the master version of the problem where everything was collapsed down into that one line of code <code>this.breakIntoFragments();</code>

which refers to a 'function' called breakIntoFragments() that handles that task.  Then we change that function to break asteroids into 2 peices instead of 3.  And we should be good to go.  

![image](https://user-images.githubusercontent.com/12129459/132723394-b3669bd0-73a1-42d4-bd49-3a5aaac816d4.png)

This is what mine looks like after deleting the conflicting sections. <br>

Save and quit that text editor.  <br>
<hr>

Notable that my Git Bash prompt tells me that I am in the middle of a Merge.  (Which I have to stage and commit to finalize).  

![image](https://user-images.githubusercontent.com/12129459/132723650-cd2b0224-76ce-4228-9574-36a31a6ad752.png)

<hr>

I will then **stage my new and improved game.js file** with the conflicts (and conflict markers) deleted. 

<code>git add game.js</code><br>

It is now ready to commit. 

### #30 Committing the Conflict Resolution

If you have been following along so far, running git commit SHOULD open a text editor with a suitable commit message already supplied for you. 

<code>git commit</code><br>

![image](https://user-images.githubusercontent.com/12129459/132724096-1eb64cfd-abab-4034-8783-bdd02a546cc4.png)<br>
<hr>
After that is complete, my Git Bash prompt no longer shows uncommitted changes (with the asterisk) or that there is a MERGE in progress.  Everything on the easy-mode branch looks good.  We can test that out by running the game and seeing if it is in-fact in easy mode (asteroids split into 2's not 3's) AND seeing if there are coins in the game (from the master branch).  <br>

To start the game from your asteroids folder you can type<br>

<code>start index.html</code>

### #30 Quiz 

The output of <code>git log</code> no longer shows that there was a problem merging.  

![image](https://user-images.githubusercontent.com/12129459/132725439-72ddaf46-60f6-4fff-a892-297c1763e5ef.png)

So don't worry if your answer doesn't match theirs. 


