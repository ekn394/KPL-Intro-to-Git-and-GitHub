# Student Questions

## Lesson 4

<hr>

## #Warning: LF will be replaced by CRLF...

![image](https://user-images.githubusercontent.com/12129459/132780869-73dc25b1-688c-4b52-9a64-80d9cc6eecc7.png)

This might be unique to me, but I am ALWAYS getting the same warning message about "LF will be replaced by CRLF" ... blah blah blah.  This has to do with the way Windows computers vs Unix/Mac/Linux computers treat text files. Creating a text file on a Windows computer and then typing out the exact same content in a text file on a Mac, will LOOK the same to us humans, but they are not.  There are invisible characters that mark when you pressed Enter to go to the next line. That invisible "end of line" character is different for Windows than for Unix/Mac/Linux. Git and GitHub (for consistency sake) will save all of its records of what changes you make in the Unix/Mac/Linux 'mode'.  If you <code>git clone</code> a repository onto a Windows computer, Git will automatically reformat it, right then and there, into Windows mode.  A real life example demonstrating this, happened to me recently. I wrote some software on a Windows computer and upload it to GitHub.  Github then saved that work in the cloud using Unix/Mac/Linux line endings (which again, are invisible to us).  When I used <code>git clone</code> to get that software onto a another Windows computer, Git reformatted it to be Windows compatible.  When I put that software onto a USB stick, and plugged it into a Mac, the software would not run due to errors AT THE END OF EVERY LINE.  HOWEVER, when I used <code>git clone</code> to download the software from GitHub *onto that same Mac*, Git/GitHub downloaded and created the clone of my repository with the proper formatting and it worked just fine.   

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

## #13 Adding a new recipes to the repository

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

## #13 Cont.  Push your changes. 

![image](https://user-images.githubusercontent.com/12129459/132953313-bccdb350-3260-4e3a-9956-feaa13b68425.png)

If you have made changes to the GitHub repository more recently than you cloned the repo onto your local computer, 
GitHub will recognize this and not allow you to push changes since you were not working from the most up to date version of the GitHub repo.  
We haven't got to this yet (this will be covered starting in #15, where you will cause this error on purpose), but for now the way to get out of this bind is to type <code>git pull</code> to pull down any changes from the GitHub version to update the copy on your local computer.  Now your local version has the most up to date Git Hub commits, AND it also has your recent local changes (making a new recipe file).  Your local copy is still ahead of where your GitHub repo is (only your local copy has your new recipe).  So you can (and should) resume the instruction to <code>git push</code> your new changes to GitHub to make sure everything is in sync again. 

<hr>

## #18 Simulate Sarah's Changes

![image](https://user-images.githubusercontent.com/12129459/132954243-a296c849-66c4-462d-8909-cdac9cc013cf.png)

Right click, Save link as... on the sarah_changes.sh

<hr>

That file saved to my Downloads folder.  <br>

![image](https://user-images.githubusercontent.com/12129459/132954411-69f56923-d5a5-42b1-bb6e-e1afd1f01184.png)


<hr> 

A shortcut to getting Git Bash to that location could be to right click anywhere in that folder (not in the icon, but anywhere else in the folder) and select Git Bash Here from the drop down menu. 

![image](https://user-images.githubusercontent.com/12129459/132954465-a42ac9d8-e148-4964-b906-4be56cab9aae.png)

<hr>

This will bring your Git Bash program to the proper spot.  

![image](https://user-images.githubusercontent.com/12129459/132954507-c7ba2987-254e-4b32-acbe-6a14cb676f14.png)

<hr>

Then substituting in your recipe url address on the end...

<code>bash sarah_changes.sh https://github.com/ekn394/recipes

![image](https://user-images.githubusercontent.com/12129459/132954772-90f8ce47-9664-472c-ad8b-d6116d9fbc17.png)

If you get an error that says "sarah_changes.sh: Did not receive enough arguments.  Expected exactly 1." 

That means you didn't include the url address to YOUR github recipes repository. 
  
<hr>
  
Then if you go look at your recipes repo on GitHub, you SHOULD see that one of the instructors, has made an update to the **GitHub version** of your recipes repo.  

![image](https://user-images.githubusercontent.com/12129459/132954692-3111c1e6-8d88-4931-810c-504563537501.png)

!!! Awesome, (a bot equivalent of) Sarah from Udacity made a commit to one of my GitHub repos!

<hr>
  

## #19 Updating Local Copies

A lot of things where thrown at you in #19 and I think another visualization would be helpful. 

<li>I followed the instructions and updated one of the spices in the chili recipe and committed it locally, but, as instructed, <em>have NOT</em> pushed that change to GitHub.  </li>

<li>I ALSO followed the instructions to have a simulated Sarah Bot, remove cumin from the chili recipe.  </li>

<li>I THEN followed the instructions to FETCH, not pull, FETCH the updates from GitHub.  This means that the 'origin/master' branch on my local computer has been updated with any new GitHub changes (removed cumin).  That 'origin/master' branch has not yet been merged with my local 'master' branch where the most recent change was me updating (in my case) salt to seasoning salt (the exact change isn't important).  </li>
  
<hr>
  
If I am on the master branch (your prompt should say master at the end) and use git log to see what the most recent change was, I will see that the most recent commit (to that branch) is me updating the spice instructions as per #16.  <br>

![image](https://user-images.githubusercontent.com/12129459/132956335-4724856d-2ba7-43b6-833d-268c6c114356.png)<br>

HOWEVER <br>
  
If I switch to another branch, the origin branch... <br>

<code>git checkout origin</code><br>
  
  ...and run <code>git log</code><br>, I will see a different, most recent commit, from Sarah about removing cumin. <br>

![image](https://user-images.githubusercontent.com/12129459/132956394-af9afece-416d-4b33-a748-77b774294549.png)

<hr>
  
You don't actually have to checkout the branches to view their git logs. 

  <code>git log master</code><br>
  and<br>
  <code>git log origin</code>
  
Will also show that they are different. <br>
  
<hr>
  
In a previous lesson we learned how to view a graph representation of the different branches. 
  
  <code>git log --graph --oneline master origin</code>
  
  This will show the **graph** (tree) structure, where each commit is only **oneline** for the branches **master** and **origin**. 
  
![image](https://user-images.githubusercontent.com/12129459/132956502-0295b0d0-70d5-430b-a58a-21856b9e562e.png)

None of this is necessary for the assignment, but I think it is helpful to see that at the top of the commit tree, I have two different universes (branches) on my local computer.  

If you are following along, don't stress out if **HEAD** is in a different spot for you.  **HEAD** just represents which branch you have checked out.  This represents the branch that new commits would be added to.  

If I change the branch that I am on to master... <br>

  <code>git checkout master</code><br>
  
Then **HEAD** appears on the master branch. <br> 

  ![image](https://user-images.githubusercontent.com/12129459/132957268-5417d781-3b20-46d9-9a65-c58e5811cc2b.png)

<hr>
  
