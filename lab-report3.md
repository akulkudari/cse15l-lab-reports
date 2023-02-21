# Lab Report 3
## The find command
For this lab report, I decided to research the find command. I found 4 modifiers for this command that can alter the way it works. 
\
\
The first alteration to the find command is the "-type" modifier. Adding this after the find command with the argument you pass through, makes it so that the search for that argument will return only results that match the type you specified. For example. If in the docsearch directory, we were to run 'find "written_2" -type d' it would only return the directories within written_2. I found this at the following [link](https://adamtheautomator.com/bash-find/#:~:text=The%20Bash%20find%20Command%20101,-Finding%20a%20file&text=The%20find%20command%20allows%20you,a%20folder%20on%20your%20computer.)
![image](https://user-images.githubusercontent.com/122570367/220237731-1bdb0918-1269-4935-93ff-168c961242b3.png)
\
If we do the same with the ending being "-type f" we get a similar result but for files.
![image](https://user-images.githubusercontent.com/122570367/220239400-25c1fdf5-0a4c-4760-9a95-31ca5628ffc2.png)  \
Another alteration I found to use on the find command is the "-depth" operator. It returns the regular output of running -find and also returns the parent directory. I found this at the following [link](https://adamtheautomator.com/bash-find/#:~:text=The%20Bash%20find%20Command%20101,-Finding%20a%20file&text=The%20find%20command%20allows%20you,a%20folder%20on%20your%20computer.) \
![image](https://user-images.githubusercontent.com/122570367/220240333-33127884-973e-458b-94d0-7058c9369d53.png)  

If we were to combine -depth and -type the result would be like this: \
![image](https://user-images.githubusercontent.com/122570367/220240469-9fc44334-360c-4369-957e-f1ed91ac8997.png)  
The -maxdepth function makes it so that the depth of the results displayed can be set by a parameter. for example, in the image below we set the maxdepth to 2. I found this at the following [link](https://adamtheautomator.com/bash-find/#:~:text=The%20Bash%20find%20Command%20101,-Finding%20a%20file&text=The%20find%20command%20allows%20you,a%20folder%20on%20your%20computer.) \
![image](https://user-images.githubusercontent.com/122570367/220242865-00f96d61-2588-433b-905e-938a5cc44827.png) \
If we were to set the maxdepth to 1 however, we would get this:
![image](https://user-images.githubusercontent.com/122570367/220242896-105f7ef3-accf-4b82-a44d-8642a7539519.png) 

Since we put the number 2 in the first image as our maxdepth, it only returned the 2 most "shallow" files or directories. The "." at the beginning means it is in the current directory, which is set to written_2. When we set the maxdepth value to 1, it only returned the files that were 1 level deep, and doesn't return their subdirectories. 
\ 
The final modifier that I was able to find for the find command was the -empty modifier. This one is quite simple, it returns all files and directories that are empty. for the sake of this example, I created 2 new directories within written_2/travel_guides, example, and exampleEmpty. I filled example with 2 files that were empty and exampleEmpty with no files at all. here is the result of running find -empty on travel_guides/example. 
![image](https://user-images.githubusercontent.com/122570367/220244667-917ca258-401e-4817-9df8-739af98d69f5.png) \
Now here is what happens when you run the same command on the travel_guides directory. 
![image](https://user-images.githubusercontent.com/122570367/220244437-5ad1e03f-151a-4100-b90f-801b23aca4ae.png) \
It returns both the empty files within example, and the empty directory. 







