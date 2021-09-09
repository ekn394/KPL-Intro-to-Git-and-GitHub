<H2> How to change the Git Bash prompt to show an * (asterisk) when there are uncommitted changes</H2>

First, open up Git Bash.

![image](https://user-images.githubusercontent.com/12129459/131062622-e040a4ca-1b54-4063-aa46-682e58dcfa22.png)

<hr>

Change the directory to the "/" folder. 

**cd /**

![image](https://user-images.githubusercontent.com/12129459/131062716-624f6c61-8327-4521-bc5b-801616626048.png)

<hr>

**ls**

When you type **ls** to list the contents of this folder, you should see a folder called _etc/_   

![image](https://user-images.githubusercontent.com/12129459/131062899-350d25c0-55be-4138-9a32-1d3402edb502.png)

<hr>

You can open up the _etc_ folder by typing 

**start etc** 

![image](https://user-images.githubusercontent.com/12129459/131063201-bf787e38-194c-4e5b-abf8-73f99a628272.png)

From there, you want to double-click on the folder named _profile.d_

<hr>


![image](https://user-images.githubusercontent.com/12129459/131063529-e98612d6-8b7e-411e-84a4-86ad7b705d5f.png)

In the profild.d folder, there should be a file named _git-prompt.sh_ that we will want to modify.
This folder is marked as 'read only' so you can't directly edit this file here (unless you change the permissions for this folder, or move the file to another location, change it there, and then move it back).  In class, we went with the option to move the file, change it, and move it back (for no particular reason).  

Drag the git-prompt.sh file from where it is, onto the desktop.  You may get a warning, just hit the _Continue_ button. 

![image](https://user-images.githubusercontent.com/12129459/131063850-3a89e8a4-a80f-4468-890b-d7758ba05dc5.png)

<hr>

From the desktop, you should now be able to right-click on the _git-prompt.sh_ file, and select **Open with** and then select **Notepad**.  You could also open this file in your favorite plain-text code editor (Visual Studio Code, Sublime Text, Notepad++, Atom).   

![image](https://user-images.githubusercontent.com/12129459/131064153-0ade20d3-ed0d-485f-8340-49607395ce9d.png)

<hr>

At the bottom of this file, add the following line 

export GIT_PS1_SHOWDIRTYSTATE=1

Save the file (CTRL-S, or take the long way, File > Save)  

<hr>

Now drag the new and improved git-prompt.sh file back into the folder where you found it.  Unless you changed where Git was installed, it is most likely found in C:\Program Files\Git\etc\profile.d

Again, you might get a warning pop-up when you drag the file back into that profile.d folder, but just click Continue again if that comes up.  

<hr>

Almost done.  Close your Git Bash program.  That git-prompt.sh file that we modified runs when Git Bash starts up, so to see the changes, we need to close Git Bash and re-open it. 

<hr>

Now, in a new Git Bash window, if you navigate to a git-enabled folder such as the 'asteroids' example from class, if there are any changes in that folder that have **NOT** been committed, you will see an asterisk * symbol at the end of the prompt.   

![image](https://user-images.githubusercontent.com/12129459/131064859-a0f3861e-85b2-4262-98f8-01b72af25b55.png)



