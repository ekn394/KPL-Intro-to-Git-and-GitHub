# Student Questions

## Lesson 4

<hr>

## #Warning: LF will be replaced by CRLF...

![image](https://user-images.githubusercontent.com/12129459/132780869-73dc25b1-688c-4b52-9a64-80d9cc6eecc7.png)

This might be unique to me, but I am ALWAYS getting the same warning message about "LF will be replaced by CRLF" ... blah blah blah.  This has to do with the way Windows computers vs Unix/Mac/Linux computers treat text files. Creating a text file on a Windows computer and then typing out the exact same content in a text file on a Mac, will LOOK the same to us humans, but they are not.  There are invisible characters that mark when you pressed Enter to go to the next line. That invisible "end of line" character is different for Windows than for Unix/Mac/Linux. Git and GitHub (for consistency sake) will save all of its records of what changes you make in the Unix/Mac/Linux 'mode'.  If you <code>git clone</code> a repository onto a Windows computer, Git will automatically reformat it, right then and there, into Windows mode.  A real life example demonstrating this, happened to me recently. I wrote some software on a Windows computer and upload it to GitHub.  Github then saved that work in the cloud using Unix/Mac/Linux line endings (which again, are invisible to us).  When I used <code>git clone</code> to get that software onto a another Windows computer, Git reformatted it to be Windows compatible.  When I put that softare on a USB stick, and plugged it into a Mac, the software would not run due to errors AT THE END OF EVERY LINE.  HOWEVER, when I use <code>git clone</code> to download the software from GitHub *onto that same Mac*, Git/GitHub downloaded and created my clone of the repository with the proper formatting and worked just fine.   

Q: How can I disable this warning? 

<code>git config --global core.safecrlf false</code>

![image](https://user-images.githubusercontent.com/12129459/132780928-88203eea-51af-4978-9c50-4c8f59796308.png)

All better now.  

<hr>

## #5 - "Post a link to the forums"

When they say 'post a link to your github reflections' in the forums, ignore that. This is no longer an active course at Udacity, (i.e. if you search the Udacity course catalogue you will not find it), so there is no forum anymore.  Udacity does has a more modern class about Git, but it wasn't as comprehensive (doesn't include GitHub), so I went with the old course that you can only get to if you happen to know <a href="https://classroom.udacity.com/courses/ud775" target="_blank">the URL</a>. 

That might also answer some of your questions about why there are out-of-date things in this course.  Yes there are, but this is still the best resource (and free) for learning about Git and GitHub that I have stumbled accross.   

<hr>

## #6 Adding a new file button has changed

![image](https://user-images.githubusercontent.com/12129459/132923875-8cc4a757-7e6a-4335-bf7c-79645ad7d3f0.png)

In the video they show adding a file to GitHub by pressing a '+' plus sign.  

<hr>

![image](https://user-images.githubusercontent.com/12129459/132924009-2263b2ff-b972-4509-ab30-6899f2410e3f.png)

The option to create a new file is now found under a drop down menu labeled "**Add file**".

<hr>

## #12 Forking the Recipes Repository


![image](https://user-images.githubusercontent.com/12129459/132950367-fabae6fd-b157-4801-8af9-c99540c15471.png)


In the video they show the url for cloning the repository on a right hand side menu.  

<hr>

![image](https://user-images.githubusercontent.com/12129459/132950481-ec9ecc23-dff0-49f6-816e-4c25898ac32b.png)

This right hand side menu has changed and no longer shows the url for the repository.  There is a gear icon that will open up a popup that shows the url for the repository. 

<hr>

![image](https://user-images.githubusercontent.com/12129459/132950520-3ac1be41-a295-45df-9750-566ddaabbda6.png)

However, I think it is even easier to just copy the address from the address bar at the top of your web browser. 

<hr>

## #13 Push Changes to the Recipes Repository

![image](https://user-images.githubusercontent.com/12129459/132951519-cd353c83-2bef-4008-8ac3-631c0d9b9a19.png)

That one line of instructions above has *many* steps that you might have forgotten about if it has been a week since Lesson 3.  <br>

Creating a new text file of a recipe.  <br>

<code>code myRecipe.txt</code><br>

![image](https://user-images.githubusercontent.com/12129459/132951613-27b09392-584d-4aa8-a664-f1d30b925529.png)

Type in your recipe (real or fake), and save the changes to that text file.  <br>

Now that you have made a substantial change in our repository, we will want to make a commit. 

Before I make any commit, I use <code>git status</code> to see what changes I have made, just in case I made changes in the past that I forgot about. 

![image](https://user-images.githubusercontent.com/12129459/132951662-cfc4ac2b-b386-4ed3-aa9c-a20ec93670bb.png)

<hr>

That looks fine, I will add my new recipe to the staging area with <code>git add</code>

![image](https://user-images.githubusercontent.com/12129459/132951696-24f5785b-05f4-44df-bd8a-9d27074bcb0c.png)

<hr>

Finally I will use <code>git commit</code> to commit it, I will be prompted to give this commit a commit message, where I said "Added recipe for nuts-n-bolts".  

And NOW I have made it to the end of that one line of instructions.  I understand that the course (rightly so) is designed to hand-hold us  less and less as we go, but just in case you forgot all of the mini-steps that go into that particular instruction, there you go.  


