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
  
  <h2> #19 Updating Local Copies </h2>

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
  
  This will show the **graph** (tree) structure, where each commit is summarized into **oneline**, for each of the branches **master** and **origin**. 
  
![image](https://user-images.githubusercontent.com/12129459/132956502-0295b0d0-70d5-430b-a58a-21856b9e562e.png)

None of this is necessary for the assignment, but I think it is helpful to see that at the top of the commit tree, I have two different universes (branches) on my local computer.  

If you are following along, don't stress out if **HEAD** is in a different spot for you.  **HEAD** just represents which branch you have checked out.  This represents the branch that new commits would be added to.  

If I change the branch that I am on to master... <br>

  <code>git checkout master</code><br>
  
Then **HEAD** appears on the master branch. <br> 

  ![image](https://user-images.githubusercontent.com/12129459/132957268-5417d781-3b20-46d9-9a65-c58e5811cc2b.png)

<hr>
  

 Something else that we skipped over in Lesson 3, that now makes more sense is the 'origin/master' label on our tree diagrams. 
  
Just as an illustration, I'm going to cd my way back to the asteroids folder and then checkout the master branch 
  
  <code>cd ..</code> <br><br>
  
  <code>cd asteroids</code> <br><br>
  
  <code>git checkout master</code> <br><br>
  

  If we run <code>git status</code> here, we will see that message that tells us that the local master branch is ahead of the 'origin/master' (the last time we used GitHub on the master branch) by 7 commits.

 ![image](https://user-images.githubusercontent.com/12129459/132960326-43819ee5-6a7a-46b2-880d-07294df9ded9.png)

<hr>

  Running <code>git log --graph --oneline</code> will show us the tree structure (according to the master branch). This does show the 7 commits since the origin/master was last updated.

![image](https://user-images.githubusercontent.com/12129459/132960441-cd3344b6-e060-4734-817a-ecdb8edc64ab.png)

<hr>
  
Note, that easy-mode is a separate branch from the master.  If we want to see a tree structure that includes it we could instead say <br>

  <code>git log --graph --oneline easy-mode</code>
  
  This gives us a larger set of branches and commits.  

![image](https://user-images.githubusercontent.com/12129459/132960636-c0053ef5-a868-41c7-8c03-25a10b36ad40.png)

  I find it easier to draw them a slightly different way (by hand). 
  
  ![image](https://user-images.githubusercontent.com/12129459/132960866-2638dd14-b30a-42a7-83f3-09da01ed20b7.png)

Where:<br>
  <li>blue arrows represent changes on the 'coins' branch. </li>
  <li>yellow arrows represent changes on the 'master' branch.</li>
  <li>red arrow represent changes on the 'easy-mode' branch.</li>

<br>  
That was a large side note, but point of the story is that the 'origin/master' label indicates the last time that our local 'master' branch was synced to the "origin" master (a.k.a. the master branch on GitHub).  
  
The 'origin/coins' label indicates the last time that our "coins" branch was synced with its 'origin' (a.k.a the coins branch on Github). 

<hr>
  
## #20 - Merging the changes
  
![image](https://user-images.githubusercontent.com/12129459/132974555-4fbda119-5259-4a2a-8c9e-5f119f080526.png)

  At this point, master is different from origin/master. The one that is synched with GitHub (origin/master) contains the cumin subtraction, and the local master has seasoning salt substitution.  

At one point both of these changes modify the same line from their mutual common ancestor commit.  Since it is changed in two different ways, this will cause a merge conflict.  
  
Attempting to merge them with <br>
  
  <code>git merge master origin/master</code><br>
  
  ![image](https://user-images.githubusercontent.com/12129459/132974654-87dac613-a795-4994-95e6-a44754b04185.png)

  We see that there is a conflict in the file named chili-recipe.txt <br>
  
  Open it up with <code>code chili-recipe.txt</code>
  
  There will be three versions, the two new (and conflicting) versions, and an old version before either change.  Delete two of the three versions, including the lines that mark the separation of the three sections. Then save and quit that file.  
  
  You now have a modified file *chili-recipe.txt* so you will need to add it to the staging area to commit those changes. <br>

  <code>git add chili-recipe.txt</code> <br>
  
  <code>git commit</code>
  
  Close the code editor when you are happy with the commit message (one will be supplied for you indicating a merge). 
  "Merge remote-tracking branch 'origin/master'"
  
  <hr>
  
You can now push your up to date master branch to GitHub (origin), which will put the local and the GitHub versions in sync.  

  <code>git push origin master</code>
  
## #23 - Making a Pull request
  
  So much happens in this video that it is tempting to give up here.  But it is a series of easy steps.  
  
First of all you will need to edit your cake-recipe.txt 
  
  <br><code>code cake-recipe.txt</code><br>
  
  Then after making and saving some change (vegetable oil to canola oil for example), enter the Git Bash commands as shown in the video. 

![image](https://user-images.githubusercontent.com/12129459/133110973-f912030b-1f4d-4809-bdc4-0c486141b19d.png)

  To make it a bit easier to read, here are those instructions one at a time. <br>
  
  <code>git branch different-oil</code>  <em>This creates a new branch (a new alternate reality) </em>
  
<code>git checkout different-oil</code>  <em>This checks out that new branch (new commits will go on that branch ) </em>
  
<code>git add cake-recipe.txt</code>  <em>Add our updated cake-recipe to that new branch </em>
  
<code>git commit</code> <em>Freeze the state of this branch in case we ever want to get back to this point. </em>
  
<code>git push origin different-oil</code>  <em>Send this alternate branch up to GitHub (as an alternate branch)</em>

<hr>
 
Next head over to your recipes repository on GitHub. <br>
  
  By default GitHub will show you the 'master' branch as opposed to other experimental branches, but you can click the drop down menu to select a different branch.  

 ![image](https://user-images.githubusercontent.com/12129459/133113193-c9f4e357-695f-44a8-83b2-9008baff07d4.png)

  <hr>
  
  ![image](https://user-images.githubusercontent.com/12129459/133113374-a7046aa1-4ff3-42c1-90e2-e06b60203ef6.png)

  From that drop down menu, you should see a checkmark beside the branch that is "checked out" on GitHub.  
  
  Select your alternate branch 'different-oil'.  As the video said, this is the GitHub (cloud) equivalent to running git checkout different-oil on your local machine.  

  <hr>
  
  There should be a Pull requests button just above where you select the branches. 
  
  ![image](https://user-images.githubusercontent.com/12129459/133114241-0b25ab87-f357-4e18-9a56-65dac984486b.png)

Click on that Pull request button. 
  
<hr> 

![image](https://user-images.githubusercontent.com/12129459/133114461-b5db13b9-bdf4-4f7c-8359-616fae30c380.png)

  This will bring you to a page where you can manage and see all of the pull requests regarding this repository.  
There ... probably aren't any yet, but you can click the green button labeled "New pull request" to create one.  

<hr>
  
![image](https://user-images.githubusercontent.com/12129459/133115390-3b88930d-f78a-4a62-9bae-d21bde9a2923.png)


By default, when you are making a pull request, it ASSUMES that you want to submit your changes to the Main master branch OF THE ORIGINAL (by some guy named Larry!).  This is NOT what we want.  We want to submit our update to our own fork of recipes. 
  
  <hr>
  
  ![image](https://user-images.githubusercontent.com/12129459/133115786-05d330e1-9fb1-4060-8bc2-279b558c1b8c.png)

  On the first drop down, about which fork you want to submit your changes too - I will select my own fork of recipes from the list of 20,000 people who have forked Larry's recipe repository.  20,000!  Wow, where did all those come from?  Well, we are not the first people going through this Udacity course. 20,000 people have made it far enough in this course to have successfully forked the recipe repository.  Anyways.  

In the first drop down select your own fork. 
yourName/recipes  it SHOULD be the 2nd item in the drop down list, after the original. 
  
<hr>
  
![image](https://user-images.githubusercontent.com/12129459/133117836-39973438-ab93-4cdc-941e-5ba6c4547f5b.png)

  After changing that first drop down to be my fork of recipes.  The pull request thinks that I am trying to merge my master branch with my master branch, so it doesn't think there is anything to do.  

On the second drop down menu, select your 'different-oil' branch. 

  <hr>
  
  ![image](https://user-images.githubusercontent.com/12129459/133117085-4dc3557e-91d3-4c59-bc89-018deca9a184.png)

  Now, this is more like it.  I can see the changes I am requesting be put into this repository.  (It HAPPENS to my repository anyways, but these are the steps you would take to suggest an update to someone elses repository.  (Ahhhhh THAT'S why we are making this change this way.  This is how multiple people could collaborate on a shared project, making change submissions (called "pull requests").
  
  <hr>
  

![image](https://user-images.githubusercontent.com/12129459/133119628-fa0229ab-dfe3-4b21-ae0d-7a84a487ba23.png)

  After you click the green button to create a pull request, you are brought to another screen where (as is tradition) you are asked to write a brief message explaining the purpose of this change.   

After you have your short explanation done, hit the green "Create pull requets" button and hope for the best. 

<hr>
  
  Now when I look at my GitHub page for my recipes repository, I can see that there is one pull request.  I wonder who it's from?!
  
  ![image](https://user-images.githubusercontent.com/12129459/133120142-6ad703ce-a355-4c5e-b95b-efef2bbcee42.png)

<hr> 
  
  <h1> The quiz at the end of #23, is bugged in a few ways.</h1> 
  
  Their video explanation has a mistake, that they address in text below the quiz.  But... I still feel like one of the answers is still wrong.  I am no expert though.  I feel like the staging area 'gets changed' whenever a commit is made, because the staging area goes from having items staged to not having items staged.  So I feel like that column SHOULD have a check box.  But the quiz doesn't think so.  I could be wrong.  In conclusion, don't stress out about the quiz too much.  
  
 <h1> #27 - Change to the local master branch before pulling changes from GitHub</h1> 
  
After doing some magic in #26, where bot Sarah updates your master branch in GitHub to have 3/4 cup of oil instead of 1/2, 
  You are asked to update your local master branch with a <code>git pull origin master</code> (pulling down the master branch code from GitHub)
  
  <h3>HOWEVER</h3>
  
 On your local machine you are probably still on the different-oil branch.  So you will FIRST need to checkout the master branch.  

  <code>git checkout master</code>
  
  IF you forgot this step (as I did), and you tried to pull down the master branch from github, you will get a merge error (and not the one we are expecting a little later).  To cancel this mistaken merge in progress, <code>git merge --abort</code>
  
  Okay, now going to check out the proper branch on my local computer. 
  
  <code>git checkout master</code>
  
  and THEN pull down the master from GitHub (which Sarah bot has recently updated). 

  <code>git pull origin master</code>
  
  <hr>
  
  Following the instructions, next we are supposed to checkout the different-oil branch and merge the new and improved master branch into it.  

  <code>git checkout different-oil</code>
  
  <code>git merge master different-oil</code>
  
  NOW we will get that same error message, but at least this time we can follow along with the videos, by getting the error at the right time. 
  
  The error tells us that the problem is in the cake-recipe.txt file.  So let's open that up and see what the trouble is. 
  
  <code>code cake-recipe.txt</code>
  
  <hr>
  
  ![image](https://user-images.githubusercontent.com/12129459/133132758-2eaa5ae0-4d4a-4b0b-adf6-6f7795d336da.png)

  The problem is there are two versions of the oil line, and they are both updates from the original so Git doesn't know which one we want to keep when we merge them.  The answer is neither, we want a combination where we changed the word 'vegetable' into 'canola', and where we changed '1/2' into '3/4'.  So make one of conflicting lines say that.  Then delete all of the marker lines where Git indicates the problem.   
  
  Save, close the file.  
  
  Now you have changed a file in your repository so you will need to stage it before you can commit this change.  
  
  <code>git add cake-recipe.txt</code>
  
  <code>git commit</code>
