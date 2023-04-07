# Lab Report 1

This is a tutorial of how to log into your course-specific account on ieng6. To do this, you must follow these steps:

## Step 1: Reset Your Course-Specific Account Password
* Look up your course-specific account for CSE 15L here: https://sdacs.ucsd.edu/~icc/index.php
* Enter your UCSD username and PID number
* Click the button that says "cs15lsp23zz" (the zz will be different and unique to you)
* Click the link that says "Global Password Change Tool"
* Click the link that says "Proceed to the Password Change Tool"
* In the box that asks to enter your username, type your course specific one (cs15lsp23zz), NOT your UCSD username
* Click the link that says "I want to reset my course-specific account password"
* Verify the Duo Authentication
* Confirm your email address and click the link in your email that says "UC San Diego Password reset page"
* Follow the steps to reset your password


## Step 2: Install Visual Studio Code
* Go to the Visual Studio Code website https://code.visualstudio.com/, and follow the instructions to download and install it on your computer. There are versions for all the major operating systems, like macOS (for Macs) and Windows (for PCs)
* When it is installed, you should be able to open a window that looks like this (it might have different colors, or a different menu bar, depending on your system and settings):

![vscode](https://user-images.githubusercontent.com/88350907/230518209-3cb4f5ad-89f8-4813-9d8b-59ac5ed7cc53.jpg)


## Step 3: Remotely Connect
In order to use Visual Studio Code or the terminal to connect to a remote computer over the Internet:
* Install [Git for Windows](https://gitforwindows.org/)
* Once installed, use the steps in [this post](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994) to set your default terminal to use the newly-installed git bash in Visual Studio Code
* Then, to use ssh, open a new terminal in Visual Studio Code
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


## Step 4: Run Some Commands
