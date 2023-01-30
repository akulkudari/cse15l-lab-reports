# Lab Report 1
Hello incoming CSE15L student! Today we will  be going over how to create a course specific account from ieng6.ucsd.edu, and to log into a remote computer using git bash. 
## Account Setup 
First, you're going to need to set up your account. Go to \
https://sdacs.ucsd.edu/~icc/index.php \
and lookup your account using your TritonLink username and PID. \
\
Then, you're going to reset your password to your account following [THIS](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit) tutorial. The password will take a bit to set in, so feel free to go to the next steps in the meantime.
## Installing VSCode
The first step in this process is installing and logging into Microsoft Visual Studio Code. You can install VS Code from  [here](https://code.visualstudio.com/).\
Go to the Visual Studio Code website and follow the instructions to install the software on your system. 
Once installed, you should see a screen like this: 
![Screenshot 2023-01-15 084100.png](https://raw.githubusercontent.com/akulkudari/cse15l-lab-reports/adab397c8c831d2a70f789dbb9edd24a421e2a5d/Screenshot%202023-01-15%20084100.png){: width="100%" }\
I have the dark theme on and I was working on a project earlier so it might not look exactly like this but there should be a "Getting started" page.
## Remotely Connecting
Now that we have VS Code installed, we can get to work on remotely connecting to the server using git bash. The first step is to install  [Git for Windows](https://gitforwindows.org/). \
Once you have it installed, you need to set VS Code to use the bash terminal, so follow the instructions on [this](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994) page.\
Then, open a new terminal in VS Code that looks like this ![terminal.png](https://raw.githubusercontent.com/akulkudari/cse15l-lab-reports/main/terminal.png)
Now we need to remotely connect to the server, so using your ieng6 username you got from the Account Setup step, type in the following to the bash terminal: \
ssh cs15lwi23zz@ieng6.ucsd.edu \
\
Make sure you replace the "zz" part with the unique sequence of characters for your username. You will then be prompted to enter your password, and the characters might not show up when you are typing them, this is normal. If you get a repeat of the password prompt or access denied, and you know you typed the right password, you may just have to wait a bit longer for the password to reset. \
\
You might get the following message when trying to login for the first time\
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.\
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.\
Are you sure you want to continue connecting (yes/no/[fingerprint])? \
\
Just say "yes" for this.\
\
Then, you will see something like the following: \
\
![terminalsuccess.png](https://github.com/akulkudari/cse15l-lab-reports/blob/main/terminalsuccess.png?raw=true)\
\
Once your terminal is up and running try a few commands. Some suggested important commands are: \
cd \
cd~ \
cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/ \
cd with a path to a local file 
\
It should look something like this.
![commands.png](https://github.com/akulkudari/cse15l-lab-reports/blob/main/commands.png?raw=true)

