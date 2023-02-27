# Lab Report 4
## Steps 1-3
![image](https://user-images.githubusercontent.com/122570367/221380350-98414cc3-3a3d-42bb-9d6a-de56d358d7eb.png)
I deleted the fork of the lab 7 repository. I had existing on my computer
![image](https://user-images.githubusercontent.com/122570367/221380496-031cafd5-ff8a-4bfa-b575-cfe2727dd661.png)
I recloned the lab 7 repo, and opened it in VSCode.
Step 4) 
![image](https://user-images.githubusercontent.com/122570367/221380609-e8f2a628-494f-43d6-a44f-206b3d46b0c1.png)
![image](https://user-images.githubusercontent.com/122570367/221380652-edd0f137-8c38-4eb5-8a6e-0ab300538e9c.png) \
First, I go to terminal, and click New Terminal under the dropdown menu 
![image](https://user-images.githubusercontent.com/122570367/221380756-df69b3a8-b2c9-4235-8575-b6d9d6b25573.png)
Once in the terminal, I typed in my email for ieng6.ucsd.edu, and pressed `<enter>` to execute the command
![image](https://user-images.githubusercontent.com/122570367/221380804-a48ba354-44f1-401c-91f7-d18d1d7dfccc.png)
The following was output, and since I already had set up an SSH key for my account, it automatically logged my device in without the need for me to put in the password.
Step 5) 
![image](https://user-images.githubusercontent.com/122570367/221380947-928d6786-fc90-43c9-b47a-19c65264de31.png) \
Since I had previously added a github ssh key, I just tested my connection to github by typing the command `ssh -T git@github.com` and pressing `<enter>` \
The terminal notified me that I was successfully authenticated to github. Then from the github repository for lab7, I copied the ssh key, and in the bash terminal I ran the following command `git clone git@github.com:akulkudari/lab7.git`, and pressed `<enter>`
![image](https://user-images.githubusercontent.com/122570367/221381396-eec73bc9-2c9e-4758-a184-9177978a3337.png) \
This was the terminal output.
Step 6) \
In order to run the tests, I executed the command `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java TestListExamples.java` and hit `<enter>`, then I executed the command `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples`. The following was outputted: 
![image](https://user-images.githubusercontent.com/122570367/221689569-51725b8b-a136-40f6-bec4-9674877e3257.png)
Step 7) \
in order to fix the code, I ran the following command: \
`nano ListExamples.java`
This prompted the following to appear in my terminal: \
![image](https://user-images.githubusercontent.com/122570367/221690450-17b11975-f98d-4030-9fa1-8281b6da6df4.png)
After this appeared, I navigated to the bottom of the terminal using the `<down>` key and holding it, and I found the following error: 
![image](https://user-images.githubusercontent.com/122570367/221690833-012ad7b1-8cc2-4c3e-8aaf-075cd69e724b.png) \
Instead of it being index1, the correct code should read `index2 += 1`, so I changed it through the terminal by holding the `<right>` arrow key, and deleting the `1`, replacing it with a `2`. The new code was the following:
![image](https://user-images.githubusercontent.com/122570367/221691603-8e05bef9-3b30-4de3-8538-af1b000c494b.png) \ 
Since the output reads `OK (2 tests)`, we know that the code works properly now. 

![image](https://user-images.githubusercontent.com/122570367/221690713-3a2210b3-a477-458f-9926-2b4df79f24fd.png)
Step 8) \
First, I compiled the new `ListExamples.java` file by running the command `javac ListExamples.java` in the bash terminal. Then, I ran the tests once more, to see if the error was fixed now, and I pressed the `<up><up><up>` and `<enter>` keys to do this since I had already ran the tester file in step 6. The following was outputted

Step 9) \ 
Lastly, I commited the file and pushed it to my github account. First, I ran the command `git add ListExamples.java` in my bash terminal, and there was no output for this command, but it notifies Git that I want to add a change to that file in the repository. Then, I ran `git commit -m "commit ListExamples.java to the repository for lab7"` to describe what my intention was. This was the output: 
![image](https://user-images.githubusercontent.com/122570367/221692778-5d5fb01b-2c44-450c-bf71-055281e5f57b.png)
I then ran `git push` to push the changes, and this was the output: 
![image](https://user-images.githubusercontent.com/122570367/221692891-452bc201-3d08-4663-abcf-65ce23f288b7.png)
Just to make sure that this was the right change, I went to my github account and double checked the file to see if the changes were made. 
![image](https://user-images.githubusercontent.com/122570367/221693051-8486e606-9447-439d-8cc0-55275bc255a2.png)
Since the code was changed here as well, I concluded that the push command worked.
