# Lab Report 1

This is a tutorial of how to log into your course-specific account on ieng6. To do this, you must follow these steps:

## Step 1: Reset Your Course-Specific Account Password
* Look up your course-specific account for CSE 15L here: [Account Lookup](https://sdacs.ucsd.edu/~icc/index.php)
* Enter your UCSD username and PID number
* Click the button that says "cs15lsp23zz" (the zz will be different and unique to you)
* Click the link that says "Global Password Change Tool"
* Click the link that says "Proceed to the Password Change Tool"
* In the box that asks to enter your username, type your course-specific one (cs15lsp23zz), NOT your UCSD username
* Click the link that says "I want to reset my course-specific account password"
* Verify the Duo Authentication
* Confirm your email address and click the link in your email that says "UC San Diego Password reset page"
* Follow the steps to reset your password


## Step 2: Install Visual Studio Code
* Go to the website [Visual Studio Code](https://code.visualstudio.com/), and follow the instructions to download and install it on your computer. There are versions for all the major operating systems, like macOS, Windows, and Linux
* When it is installed, you should be able to open a window that looks like this (it might have different colors, or a different menu bar, depending on your system and settings):

![vscode](https://user-images.githubusercontent.com/88350907/230518209-3cb4f5ad-89f8-4813-9d8b-59ac5ed7cc53.jpg)


## Step 3: Remotely Connect
In order to use Visual Studio Code or the terminal to connect to a remote computer over the Internet:
* Install [Git for Windows](https://gitforwindows.org/)
* Once installed, use the steps in [this post](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994) to set your default terminal to use git bash in Visual Studio Code
* Next, open a new terminal in Visual Studio Code
* After the $ sign, type the command `ssh cs15lsp23zz@ieng6.ucsd.edu` (the zz will be different and unique to you) 
* If this is the first time you've connected to this server, you will probably get a message like this: 
  ```
  The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
  RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
  Are you sure you want to continue connecting (yes/no/[fingerprint])? 
  ```
  This message is expected, so type yes and then press enter
  
* Enter your new password when prompted
* After you enter your password, you will now be on the remote server, and it should look something like this:

  ![Remote Server](https://user-images.githubusercontent.com/88350907/230541840-7140c749-8b63-424e-bbe4-ab631fe17d45.jpg)

Your terminal is now connected to a computer in the CSE basement, and any commands you run will run on that computer. We call your computer the *client* and the computer in the basement the *server*.


## Step 4: Run Some Commands
* Try running the following commands both on your own computer and on the remote computer after ssh-ing:
    * `cd`(**Change Directory**): Switch the current working directory to the given path
    * `ls`(**List Files**): List the files and folders in the given path
    * `pwd`(**Print Working Directory**): Display the current working directory
    * `mkdir`(**Make Directory**): Create a new directory/folder
    * `cp`(**Copy Files**): Create a copy of the given files
    * `cat`(**Concatenate**): Print the contents of one or more files given by the path

* Here are a few examples of commands ran on your own computer:

<img width="835" alt="1" src="https://user-images.githubusercontent.com/88350907/233799302-6f5a22c0-987a-46a9-a0d6-7a93f8b43cbc.png">
<img width="299" alt="2" src="https://user-images.githubusercontent.com/88350907/233799305-739bf670-9cb4-4b89-865a-38544c6abc17.png">

In these screenshots, I listed out the contents of my home directory (/c/Users/keean) and then changed my directory to the Downloads folder and listed out the contents of that folder. I then made a new folder in Downloads called "CSE 15L" and changed to that directory. Next, I printed out the working directory (/c/Users/keean/Downloads/CSE 15L), and then moved back up one directory to Downloads and copied file.txt into CSE 15L. Finally, I switched back to CSE 15L, listed the files, printed out the contents of file.txt, and did a few more list commands.

* Here are a few examples of commands ran on the remote computer:

<img width="516" alt="1" src="https://user-images.githubusercontent.com/88350907/233803070-58f90f66-7a63-4198-8e7f-e5800392057e.png">

In this screenshot, I first listed the contents of my current working directory, and then printed out the contents of hello.txt. I then printed my current working directory (/home/linux/ieng6/cs15lsp23/cs15lsp23ln), and proceeded to make a new directory in it called MyFolder. I listed out my current working directory again to show that MyFolder was in there, and then copied hello.txt over to MyFolder. I then did a few list commands in MyFolder before going back up one directory and printing out the contents of hello.txt again, but instead by using the entire path (/home/linux/ieng6/cs15lsp23/cs15lsp23ln/MyFolder/hello.txt).

* To log out of the remote server in your terminal, you can use either of these:
   * Ctrl-D
   * Run the command `exit`


**You now know how to log into a course-specific account on ieng6!**


