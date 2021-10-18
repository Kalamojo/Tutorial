Git/GitHub Tutorial

Git and GitHub are used extensively by programmers or anyone working with code. The power of the two combined makes sharing code efficient and manageable. While these two tools work flawlessly together, they are most certainly different things. Git is software that allows users to place their code into repositories and keep a working log of the changes they have made to that code. Even without GitHub, it is a remarkably powerful tool. GitHub, on the other hand, is a website that allows users to host and manage Git repositories. It also makes the sharing of these repositories much smoother.
While these tools make version control and file sharing much easier than more primitive methods, they certainly come with their own difficulties. This tutorial will show you how to clone a git repository onto your device, commit your file edits to your chosen repository branch, and then push the file back to GitHub with the updated changes. This specific tutorial only covers the Linux operating system, so keep that in mind while looking through.

1.	Connect your GitHub account
To access your GitHub repositories and make lasting changes, you need to first connect your GitHub account in your terminal. To do this, open your GitHub account in your browser. Locate your account username and email.

For me, that would be Kalamojo and kalabiprof@gmail.com. With this information, you can now configure your account in the terminal. Open your terminal by either looking for it in your apps or pressing ‘ctrl + alt + t’ (keep in mind that this pertains to Linux operating systems). Once open, type these commands, replacing Kalamojo with your own username and kalabiprof@gmail.com with your own account email:

git config --global user.name "Kalamojo"
git config --global user.email "kalabiprof@gmail.com"

2.	Create Repository
With your account now connected, you can now create your first repository. Its good practice to keep separate folders for each of your repositories. Navigate to a folder of choice. After doing so, use the command “git init” to initialize a repository.

mkdir newRep
cd newRep
~/newRep$ git init

3.	Open file in IDE
Now, after creating your repository, you can code and save files there. In the Linux terminal, you can create a new file with the touch command. You can also do this by entering your chosen IDE (what you use to edit code) or file system and adding a file. For this example, I will be using Visual Studio to edit my file.

touch newFile.py
code newFile.py

The “code” command automatically opens the file in Visual Studio. Alternatively, you can simply run your editor and open your file from there.
4.	Stage Changes
After creating your program or document, you then need to stage the changes to be committed to your repository. To do this, you will use the “git add” command.

git add newFile.py

At any given time throughout this process, it may be helpful to use the “git status” command. This does what the name implies, reporting the status of your repository and its files. You can use it after adding your file to ensure that it is staged.
 
5.	Commit Changes
To commit your changes to your repository, you can make use of the “git commit” command. Unlike staging, the commit command allows you to include a message with your file. This message is used to explain what changes you made and why, and it is generally good practice to include them in your repositories. Here is an example of a commit:

git commit -m "Created newFile to demonstrate git staging and commitment process"

6.	Create Repository on GitHub
This step could also be the first, but regardless of when it is done, it is necessary to save your repository. This is made very easy on GitHub. On your repository section on GitHub, simply select new repository, give it a title, and create it. This should bring you to the interface of your new repository.
7.	Push Files to Branch
Finally, once all your file changes have been staged and committed, you are ready to release them to your GitHub account. To do this, you will need the repository link. On the page of your GitHub repository, there should be a quick setup section. Here, select HTTPS and copy the link in the box to the right.
 
With the link copied, navigate to your terminal once more. Use these three commands to push your repository to GitHub:

git branch -M main
git remote add origin "insert link here"
git push -u origin main
If the third command asks you to use your credentials, enter them.

And voilà! If all went well, you should have your very own repository on GitHub up and running. This process has many modifications and rearranging the steps in multiple ways may also result in a successful GitHub repository. In addition, there are many other commands that were not used in the tutorial that add extra functionality. These include the checkout commands to un-stage changes, “git config -l” to make sure your account is configured, and many more.
