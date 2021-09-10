# Student Questions

## Lesson 4

### #Warning: LF will be replaced by CRLF...

![image](https://user-images.githubusercontent.com/12129459/132780869-73dc25b1-688c-4b52-9a64-80d9cc6eecc7.png)

Backstory on that warning message. I this might be unique to me, but I am ALWAYS getting the same warning message about "LF will be replaced by CRLF" ... blah blah blah.  This has to do with the way Windows computers vs Unix/Mac/Linux computers treat text files. Creating a text file on a Windows computer and then typing out the exact same content in a text file on a Mac, will LOOK the same to us humans, but they are not.  There are invisible characters that mark when you pressed enter to go to the next line. That "end of line" character is different for Windows than for Unix/Mac/Linux. Just to pick one way and be consistent about how files are SAVED, Git and GitHub will save all the git records of changes in Unix/Mac/Linux mode.  If you git clone a repository onto a Windows computer it will reformat it right then and there into Windows mode (for you automatically).  Another real life example that happened to me last month, is that if I write some software on a windows computer and upload it to GitHub.  Github will save it in the cloud using Unix/Mac/Linux line endings (which again are invisible to us). If I say <code>git clone</code> to get that software onto a windows computer, Git will reformat it for me to be Windows compatible.  If I put that file on a USB stick, plug it into a mac, it will not run due to errors AT THE END OF EVERY LINE.  HOWEVER if on that same Mac I use <code>git clone</code> to download it from GitHub it will download onto that Mac with the proper formatting and work just fine.   

Q: How can I disable this warning? 

<code>git config --global core.safecrlf false</code>

![image](https://user-images.githubusercontent.com/12129459/132780928-88203eea-51af-4978-9c50-4c8f59796308.png)

All better now.  

<hr>

### #5

When they say 'post a link to your github reflections' in the forums, ignore that. This is no longer an active course at Udacity, (i.e. if you search the Udacity course catalogue you will not find it), so there is no forum anymore.  There is a more modern class about Git, but it isn't as comprehensive.  I took the shorter, more modern one but found that the unlisted older version of the course to be much more informative.  By knowing how to find the course (having the url), we can still view the content and learn from it.  

That might also answer some of your questions about why there are out-of-date things in this course.  Yes there are, but it is still the best resource (and free) for learning these concepts that I have stumbled accross.   

<hr>

### #6 Adding a new file button has changed

![image](https://user-images.githubusercontent.com/12129459/132923875-8cc4a757-7e6a-4335-bf7c-79645ad7d3f0.png)

In the video they show adding a file to GitHub by pressing a '+' plus sign.  

<hr>

![image](https://user-images.githubusercontent.com/12129459/132924009-2263b2ff-b972-4509-ab30-6899f2410e3f.png)

The option to create a new file is now found under a drop down menu labeled "**Add file**".



