# Git/GitHub Tutorial

Git and GitHub are used extensively by programmers or anyone working with code. The power of the two combined makes sharing code efficient and manageable. While these two tools work flawlessly together, they are most certainly different things. 
	The working principle behind each of these tools is repository manipulation. Repositories are containers that store and manage data. Git is software that allows users to place their code into repositories and keep a working log of the changes they have made to that code. Even without GitHub, it is a remarkably powerful tool. GitHub, on the other hand, is a website that allows users to host and manage Git repositories. It also makes the sharing of these repositories much smoother.
While these tools make version control and file sharing much easier than more primitive methods, they certainly come with their own difficulties. This tutorial will show you how to clone a git repository onto your device, commit your file edits to your chosen repository branch, and then push the file back to GitHub with the updated changes. This specific tutorial only covers the Linux and Windows operating systems, so keep that in mind while looking through.

### Prerequisites
To make use of any Git repositories or commands, the Git software must first be installed. A guide through the installation process is available on the Git Documentation at https://git-scm.com/book/en/v2/Getting-Started-Installing-Git. 
In addition to Git, an IDE or Integrated Development Environment will be needed to create code files for your repository. If you don’t want to download some of the more popular options like Visual Studio, IntelliJ IDEA, or Atom, you can simply use your device’s notepad app to create and save files. I will be using Visual Studio in my examples, but you can use anything you feel comfortable with. To follow along with the tutorial, be ready to create some sort of program to include in the repository, or you can pre-create them.





## Instructions for Windows					->

1.	Setup GitHub Desktop
A good option for Git and GitHub control on Windows is through GitHub Desktop. This app allows users to access, edit, and release code without the use of commands and the terminal. To start using this product, download the app at https://desktop.github.com. To begin using it, you must first connect your GitHub account. Select File and then options at the menu at the top right of the window. Next, under accounts, there is an option to sign in. Select the GitHub.com option and enter your credentials.


2.	Create your repository
Under the File menu option, select New Repository, and enter the name and description. After creating it, you should be brought to a screen that displays your repository options

<p align="center"><img src="https://user-images.githubusercontent.com/64047609/143937929-8803cc8f-d320-4e03-a7e5-e976f00fd3c8.png" alt="github reposity options"></p>

For this tutorial, we are going to select the “Show in Explorer” option. Upon selection, a File window pertaining to your repository should be opened and ready to work with.


3.	Add your files to Folder
In your IDE of choice, create a program. Save the file into your repository folder.

<p align="center"><img src="https://user-images.githubusercontent.com/64047609/143938171-61bd0e22-d17b-435b-88e1-55e1da215430.png" alt="add file folder"></p>

Alternatively, you could move already existing files into the folder. When you go back to GitHub Desktop, you should see the changed files listed there, ready to be committed. 

<p align="center"><img src="https://user-images.githubusercontent.com/64047609/143938245-37b5985c-31b6-40f9-bb2d-b4bad9895eca.png" alt="git desk change"></p>


4.	Commit changes
Now it is time to commit your files to your repository. Conveniently, at the bottom-left of your screen, a commitment prompt is positioned. Include the commitment name, and description if desired, and select “Commit to main”.


5.	Publish Repository
You should be seeing the repository options screen again upon commitment. To push your repository to GitHub, select the highlighted “Publish repository” button. It will display your repository name and description once more for last-minute edits. Select the publish button again.

<p align="center"><img src="https://user-images.githubusercontent.com/64047609/143938324-ccbb6e72-e528-40a8-b5d9-eff23bf98c97.png" alt="git desk commit"></p>








## Instructions for Linux 						->

1.	Connect your GitHub account
To access your GitHub repositories and make lasting changes, you need to first connect your GitHub account to your terminal. To do this, open your GitHub account in your browser. Locate your account username and email.

![github_profile](https://user-images.githubusercontent.com/64047609/143938590-52f03efc-07b2-4227-bd7e-2c89c4110d1d.png)

For me, that would be Kalamojo and kalabiprof@gmail.com. With this information, you can now configure your account in the terminal. Open your device terminal by either looking for it in your apps or pressing ‘ctrl + alt + t’ (keep in mind that this pertains to Linux operating systems). Once open, type these commands, replacing Kalamojo with your own username and kalabiprof@gmail.com with your own account email:

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

![git_status](https://user-images.githubusercontent.com/64047609/143938676-b80e2594-dc2d-404b-a1c9-ba9a154de142.png)


5.	Commit Changes
To commit your changes to your repository, you can make use of the “git commit” command. Unlike staging, the commit command allows you to include a message with your file. This message is used to explain what changes you made and why, and it is generally good practice to include them in your repositories. Here is an example of a commit:
git commit -m "Created newFile to demonstrate git staging and commitment process"

6.	Create Repository on GitHub

![github_rep](https://user-images.githubusercontent.com/64047609/143938726-8f3893bf-66af-4473-a3c7-ef461cc61375.png)

This step could also be the first, but regardless of when it is done, it is necessary to save your repository. This is made very easy on GitHub. On your repository section on GitHub, simply select new repository, give it a title, and create it. This should bring you to the interface of your new repository.


7.	Push Files to Branch
Finally, once all your file changes have been staged and committed, you are ready to release them to your GitHub account. To do this, you will need the repository link. On the page of your GitHub repository, there should be a quick setup section. Here, select HTTPS and copy the link in the box to the right.

![github_rep_setup](https://user-images.githubusercontent.com/64047609/143938781-0c909a87-7912-4531-89d7-2b0ab7e70d41.png)

With the link copied, navigate to your terminal once more. Use these three commands to push your repository to GitHub:
git branch -M main
git remote add origin "insert link here"
git push -u origin main
	
If the third command asks you to use your credentials, enter them.










 Conclusion						->


And voilà! If all went well, you should have your very own repository on GitHub up and running. 
![new_rep_W](https://user-images.githubusercontent.com/64047609/143938859-53b184a6-a6b4-4f86-a5e4-43f5359e9db4.png)
![new_rep_L](https://user-images.githubusercontent.com/64047609/143938871-17d691ed-7bff-49da-8bce-4244a6508197.png)
This process has many modifications and rearranging the steps in multiple ways may also result in a successful GitHub repository. In addition, there are many other commands that were not used in the tutorial that add extra functionality. This tutorial only went over the basics, so feel free to visit Git or GitHub documentation at their various websites. There are also many other tutorials around that can help you accomplish your goals.

Reference Links

-	GitHub Tutorial: https://guides.github.com/activities/hello-world/
-	Git Tutorial: https://git-scm.com/docs/gittutorial-2
-	FreeCodeCamp Guide: https://www.freecodecamp.org/news/the-beginners-guide-to-git-github/
-	The Odin Project Guide: https://www.theodinproject.com/paths/foundations/courses/foundations/lessons/git-basics
