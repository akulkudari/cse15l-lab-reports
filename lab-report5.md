# Lab Report 5
## Lab Report 4: Bash Script
For this Lab Report I decided to write the bash script for lab report 4 so that all the tasks would be done with a single run of the script. 
### Step 2) Forking the Script
I did this manually 
### Step 3) Starting the timer 
I also did this manually ;)
### Step 4) Log into ieng6 
Since I had a ssh key set up, I just typed in `ssh myusername@ieng6.ucsd.edu"` I don't know how to do this without an ssh key, since you have to manually input the password. 
### Step 5) Cloning the Repository
to clone the repo from github, you just type `git clone git@github.com:yourgithubusername/lab7.git` into the bash script. We then want to navigate to the repository cloned so our next line in the bash script will be \
`cd lab7`
### Step 6) Run the tests, and demonstrate failure 
The following line will compile the tests when inserted into the bash script: `javac -cp ../libs/junit-4.13.2.jar:../libs/hamcrest-2.2.jar:. TestListExamples.java ` \
This line will run the tests `java -cp ../libs/junit-4.13.2.jar:../libs/hamcrest-2.2.jar:. org.junit.runner.JUnitCore TestListExamples` \
Here is a screenshot of the code failing: 
![image](https://user-images.githubusercontent.com/122570367/225206221-71f13b61-3290-4195-ad87-092e7e42a44e.png)

### Step 7) Changing the code 
I wrote `nano ListExamples.java` into my bash script but you need to manually fix the code since that is a bit complex for the machine to do. I fixed the error line, and reran the code after.
### Step 8) Compiling and running the code 
After nano is exited, I had the `javac ListExamples.java` command into my script next so that it would compile the new code. It was successful, and i ran the testers once more, typing in: \
`javac -cp ../libs/junit-4.13.2.jar:../libs/hamcrest-2.2.jar:. TestListExamples.java ` \
This line will run the tests `java -cp ../libs/junit-4.13.2.jar:../libs/hamcrest-2.2.jar:. org.junit.runner.JUnitCore TestListExamples` \
![image](https://user-images.githubusercontent.com/122570367/225206817-d47f269b-0f73-4682-a8d2-32fb9f11e489.png)
As we can see they run properly now 
### Step 9) Committing and pushing the file 
For this step, I used the following commands in the script: \
`git add ListExamples.java`\
`git commit -m "commit ListExamples.java to the repository for lab7"`\
`git push`\
This resulted in a successful commit, and when I double checked the github code, it was fixed: 
![image](https://user-images.githubusercontent.com/122570367/225207203-3a84623c-cf9c-48a7-8f52-762ddafc3651.png)
