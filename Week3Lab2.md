# ✨ Welcome to my Lab Report #2 ✨
------------------------------------

## Throughout this page we will review a program that I have written called "StringServer" 

# Lets Begin!

**1. The Code**
- Using NumberServer.java as a template I was able to understand how the numbers were stored into a string array and then added up them up into a single integer.
- Using those ideas I was able to construct a StringServer that allows a user to "add-messages" to the webpage so that it can keep track of any message the user may want to leave.

Here is the Code:
![Image]()
* After following the link enter your username and student id to acquire your CSE15L course specific account.
* The account will begin with the 9 digits "**cs15lwi23**" and end with a 3 digit unique identification code.
* This 12 digit name will be used to access your account on **ieng6** servers.

If you are having troubles accessing your account you can reset your password here [Password Reset](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit).

________________________________________________________________________________________________________________________________________________________

**2. Step Two**
- Download and Install Visual Studio Code

![Image](https://cdn.thenewstack.io/media/2021/10/4f0ac3e0-visual_studio_code.png)

  * Use this [Link](https://code.visualstudio.com/) to download and install Visual Studio Code and follow the instructions on page.

  ![image](https://user-images.githubusercontent.com/122570751/212203157-ac4ed01a-2f38-4263-937d-a0a5efffc4a8.png)
  
  
  * *Click on the download that best suites the Operating System on your personal device*
 
Once fully installed it should look like this...

![image](https://user-images.githubusercontent.com/122570751/212203634-2af23662-4cca-4578-9d13-faa76c3eac39.png)

> **Now you're ready to code!**

________________________________________________________________________________________________________________________________________________________


**3. Step Three**
- Connecting remotely to the ieng6 servers
  * First download [git](https://gitforwindows.org/) using the standard installation settings. **(No need to change any settings during installation)**
  * After git is finished downloading, follow the step by step instructions from this **[link](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994)**.
  * (This will allow you to set Git Bash terminal as your default terminal)
  * Great job!
 
________________________________________________________________________________________________________________________________________________________


**4. Step Four**
- Use git bash on Visual Studio Code and log in using the login creditentials we obtained in **Step One**.

In order to use git bash on VScode you first have to open up VScode and open a new terminal and verify that Git Bash is set as the Default terminal. 

![image](https://user-images.githubusercontent.com/122570751/212206604-c444d328-f691-4054-9a4f-131983279ecb.png)

________________________________________________________________________________________________________________________________________________________


Once you have the terminal ready, you're ready to login and begin testing some commands.

## Login Steps for **ieng6**
> - In the terminal in VScode type "ssh cs15lwi23___@ieng6.ucsd.edu" but make sure to replace the "___" with your unique 3 digit code that was acquired in **Step One**, then press enter.
> - If this is your first time you will recieve a message asking you to authorize your connection to the server. It should look like this...
> ```
> ⤇ ssh cs15lwi23zz@ieng6.ucsd.edu
> The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
> RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
> Are you sure you want to continue connecting (yes/no/[fingerprint])? 
> ```
> Type **Yes** and press **Enter**.
> You will then be given a prompt to enter your password, type in your password from **Step One** and press **Enter**.
> *Notice that you will not see your password being written out. This is a security feature.*
> Once logged in correctly you should see some text being displayed in your terminal similar to the photo below.
>
> ![image](https://user-images.githubusercontent.com/122570751/212208288-a6695f5e-5af2-4e35-b394-e120428238a9.png)
>

**Nice Job! You are now connected REMOTELY to a computer located in the CSE building.**
**Any commands that you enter in the terminal will be run on that computer.**

________________________________________________________________________________________________________________________________________________________


# **Want to try out some commands?**

> I recommend running some simple commands to test out the terminal and ensure that everything is running effortlessly!
> 
> **Some commands to try**
> ________________________
>
>  **Try using "pwd" command in the terminal.**
>    * pwd stands for "Print Working Directory". Which essentially prints the current directory that your are in.
>    Here is an example:
>    
>    ![image](https://user-images.githubusercontent.com/122570751/212210696-dc771b0e-09da-440d-af50-65ce2dd51545.png)
>    
>    After typing in "pwd" we are given the current working directory, which in the example is **"/home/linux/ieng6/cs15lwi23/cs15lwi23asg"**.


>  **Try using "cat /home/linux/ieng6/cs15lwi23/public/hello.txt" command in the terminal.**
>    * Cat stands for "concatenate". This command prints the contents of the path that is given.
>    In this example we are using the "/home/linux/ieng6/cs15lwi23/public/hello.txt" directory to access the contents of "hello.txt" file.
>    Here is an example:
>    
>    ![image](https://user-images.githubusercontent.com/122570751/212211661-3dd9d5dd-c977-406c-98f9-2cf50322fd65.png)
>    
>    As you can see, after typing in "cat <path>" the contents of the "<path>" are printed out and in this example we see the message.
>    "Hello! Welcome to CSE 15L"

 
>  **Try using "cd .." command in the terminal.**
>    * cd stands for "current directory". And ".." retrieves the parent directory.
>    So together using "cd .." we are given the parent directory of the current directory.
>    Here is an example:
>
>    ![image](https://user-images.githubusercontent.com/122570751/212212767-0edbebe5-b822-4d65-849b-a963d7421a39.png)
>
>    As you can see the current directory was changed to the parent directory after using the command "cd .."
>

 
> **Great Job! Check out these additional commands you can try.**
>    - cd
>    - ls -lat
>    - cd ~
>    Any idea what they do?
  
## You finished! Great Job!
