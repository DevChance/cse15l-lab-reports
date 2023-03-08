# **✨ Welcome to my Lab Report #4 ✨** 

Written by: Chance Spurlin

------------------------------------

# In this Lab Report, we will learn how to clone a repository, run, fix, and update, tests all by through using the terminal.

## We will be completing these 6 steps

**1. Log into ieng6**

**2. Clone your fork of the repository from your Github account**

**3. Run the tests, demonstrating that they fail**

**4. Edit the code file to fix the failing test**

**5. Run the tests, demonstrating that they now succeed**

**6. Commit and push the resulting change to your Github account (you can pick any commit message!)**







# Let's first begin by starting at the terminal:

![image](https://user-images.githubusercontent.com/122570751/223589550-918f6b24-0351-4dee-b693-dfa0c59759af.png)

# Now Lets Complete Each of The Six Steps:

## Step One: Log into ieng6

**1. First, we must log into the ieng6 server. To do this, we type ssh cs15lwi23___@ieng6.ucsd.edu.**

**2. You will then be prompted to enter your password, after you enter your password press [ENTER].**

**3. Now you're logged in to ieng6!**

![image](https://user-images.githubusercontent.com/122570751/223589816-992b4e95-ec31-4807-a3e0-8ec88e94c37e.png)



## Step Two: Clone your fork of the repository from your Github account

**1. First, you type git clone ______.**

**2. The blank space is where you insert your <ins>ssh clone url<ins>.**

**3. Then press [ENTER] and your github repository from your account should be cloned!**


![image](https://user-images.githubusercontent.com/122570751/223590879-1bc03dce-ecbf-4de4-b812-a725e11f118a.png)


## Step Three: Run the tests, demonstrating that they fail

1. After cloning your repository you now need to cd into lab7/.
      
2. First, type: cd lab7/ (You can type l followed by <tab> to autogenerate the rest of the file).
      
3. Now that we are in the correct directory we can begin to compile and run the java tests.
      
4. To compile we type and press [ENTER]: javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
      
5. This compiles all .java files in the current directory.
      
6. Then to run the tests we type and press [ENTER]: java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests.
    
7. This will run the **ListExampleTests** and output the results.
      
![image](https://user-images.githubusercontent.com/122570751/223592206-ffa59c7c-e8d2-4d58-953d-6968f236cfc6.png)

## Step Four: Edit the code file to fix the failing test
 
1. After running the test, we notice that there is 1 failure, this is what we are going to fix!
2. To access the test file we will type: nano ListExamples.java
3. Now that we have nano'd into the file, we will navigate to fix the bug causing the failed test.
4. Press <CNTRL> W
5. This will search through the file, then type and press [ENTER]: while(index2
6. This will bring you to the first occurence of "while(index2" then press down on the arrow key twice (<dowm> <down>)
7. This will bring you to the line containing "index1 += 1" navigate to the 1 by pressing on the right arrow key 8 times (<right> <right> <right> <right> <right> <right> <right> <right> <right>)
8. This will bring you to the number 1. Delete the number 1 in "index1" and replace it with the number 2 so it is now "index2"
9. The new line should be "index2 += 1".
10. Then press <CNTRL> X. This will prompt the terminal to ask you if you would "Yes" like to save "No" dont save.
11. Press Y for "Yes" and then it will prompt you for the file name, it should remain the same so just press [ENTER]

![image](https://user-images.githubusercontent.com/122570751/223594813-44ae60ef-703a-47ae-829e-99a22d5264f2.png)
      
![image](https://user-images.githubusercontent.com/122570751/223594973-85ee9c6e-d567-475a-8111-534d130a4225.png)   
      
![image](https://user-images.githubusercontent.com/122570751/223595100-19f7937d-e0c5-498b-ab73-7469d1f02ba9.png)

      
## Step Five: Run the tests, demonstrating that they now succeed

1. After fixing the file we now want to rerun the tests to ensure they pass succesfully after we addressed the bug.
2. After exiting nano text editor we will be at the cwd, we then want to compile all the .java files again.
3. To compile we type and press [ENTER]: javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
4. Then to run the test we type and press [ENTER]: java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
5. After running the tests we notice that the results and printed and we got "OK (2 tests)" which shows we succesfully fixed the bug!

![image](https://user-images.githubusercontent.com/122570751/223595880-f74903b8-cc4c-4e9b-acd3-2f737e9bcd60.png)

## Step Six: Commit and push the resulting change to your Github account (you can pick any commit message!)

1. After running the tests and ensuring everything passed, we want to add, commit, and push the changes to our repository.
2. To do this, first we type : git add ListExamples.java
3. This stages the changes for that file, we then type: git commit -m "Updated ListExamples.java"
4. After commiting the changes we want to push the command to our repository so we type: git push origin main
5. This push all of our changes to "ListExamples.java" to reflect on the repository on my Github account.

![image](https://user-images.githubusercontent.com/122570751/223596628-c7c25ddb-3cb6-458e-96b3-13b24f1d547d.png)

# Now lets navigate to the github repository online to see if the changes were made!

![image](https://user-images.githubusercontent.com/122570751/223596786-dd546a06-6685-4b98-98be-c1c35be92952.png)

# As we can see, "index1 += 1" on line 43 was succesfully changed to "index2 += 1" this change fixes all tests!
