# **✨ Welcome to my Lab Report #5 ✨** 

Written by: Chance Spurlin

------------------------------------

#### **In this lab report we will utilize a bash script to complete the tasks from Lab Report 4; This will greatly reduce the time and effort needed to complete the tasks!**

 * As you may recall from Lab Report 4, we were tasked to complete a total of **six steps**
 * Utilizing a bash script we are going to streamline the process and significantly reduce the number of steps required by the user
 * This will greatly reduce the time needed to complete the task and minimize the risk of user-errors

## For reference, here are the **six steps** from Lab Report 4 that we will complete in our bash script:

**1. Log into ieng6**

**2. Clone your fork of the repository from your Github account**

**3. Run the tests, demonstrating that they fail**

**4. Edit the code file to fix the failing test**

**5. Run the tests, demonstrating that they now succeed**

**6. Commit and push the resulting change to your Github account (you can pick any commit message!)**



## To greatly reduce the time to complete the tasks we will first create a bash script:

#### Assuming we are on the correct ieng6 server we can directly create a file in the terminal using nano

- First, we type: `nano Lab5Bash.sh`

![image](https://user-images.githubusercontent.com/122570751/224882630-f7245b7a-b919-4be7-bf6d-829bf8de2c43.png)

## After typing nano, a bash script file was created in the current directory named **Lab5Bash.sh**, it will now prompt the user to code the script:

### To greatly reduce the number of tasks and  time this is the bash file I created that completes the **six steps**:

```
#!/bin/bash

read -p "Please enter your ssh clone url followed by [ENTER]: " ssh_url

git clone $ssh_url

cd lab7/

javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests

echo 'Find the second occurrence of "index1 += 1" and replace it with "index2 += 1"'     
read -p  "Then type <CNTRL> X to save and quit: Press [ENTER] to continue"

nano ListExamples.java

javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests

git add ListExamples.java

read -p "Enter your commit msg then press [ENTER]: " commit_msg

git commit -m "$commit_msg"

git push origin main

echo "Great job! You finished!"
```

## We then enter that into our nano text editor:

![image](https://user-images.githubusercontent.com/122570751/224883709-93c423f1-2bdf-4b65-ac59-2872315eee18.png)

### After correctly writing the file, type: `<CNTRL> X`
### Make sure to save and keep the file name as `Lab5Bash.sh`

## Now we must make `Lab5Bash.sh` executable! To do this we must change the file permission

- To change the file permission of `Lab5Bash.sh` type: `chmod +x Lab5Bash.sh`
- This allows Lab5Bash.sh to be executable as a script.

## Now we are ready for a timed competition!

#### If we are asked to complete the steps in a efficient time we could utilize the bash script:

- In the terminal we would type: `./Lab5Bash.sh`

![image](https://user-images.githubusercontent.com/122570751/224884940-d8ac94d1-84c5-4b7a-a2c7-df09168c660e.png)

- I am then prompted to enter the ssh clone url that I want to clone so I enter: `git@github.com:DevChance/lab7.git`

#### The bash script then clones the repository and runs the tests
#### This will then produce another prompt for the user to acknowledge the changes to the file, it then says press [ENTER] to continue:

![image](https://user-images.githubusercontent.com/122570751/224885409-d3c6995e-d538-4807-8707-2c3568271e41.png)

## Edit the file using nano and [EXIT]:

![image](https://user-images.githubusercontent.com/122570751/224885516-215f08ac-d538-486e-afb2-1029a4a98f35.png)

### Then bash script reruns the tests and adds and pushes the fix for you! Then enter the commit message and press [ENTER]

![image](https://user-images.githubusercontent.com/122570751/224885781-0c405e91-8acc-4fa1-be67-805d2a27311a.png)

## Great job! Utilizing a bash script I significantly reduced the time it takes to run tests, edit a file, rerun tests, save and push the file correctly.
