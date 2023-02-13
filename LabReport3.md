# **✨ Welcome to my Lab Report #3 ✨** 

Written by: Chance Spurlin

------------------------------------

# First, we will be looking into the "grep" command & 4 alternative command-line options that utilize **"grep"**



## What is **"grep"** & how can it be applied?



- **"grep"** is a command used to search through files containing text for a specific "pattern". It will then print out the lines that contain the specified "pattern" that was found in the text that was located in the folders.



# 4 Different Ways Grep Can be Used:



## Alternative Method 1: **"-c"**



## **grep -c**
* The "-c" command counts the number of matches of the specified "pattern" that are contained in the designated files.
* For example from the "written_2", if we wanted to know the number of times "Coconut" is mentioned in each file.
* After succesfully navgiating to the currect directory, you could type "grep -r -c "Coconut"" to search rercusively through the directories and subdirectories of the current directory and print out the number of times the string "Coconut" is found in each directory and sub-directory. 

# Here are 2 different examples of utilizing "grep -c":

## Example 1: "grep -r -c "Coconut"

```

pwd

/c/Users/Chance/Desktop/CSE15L/LabReport3/skill-demo1-data-main/skill-demo1-data-main

grep -r -c "Coconut"

written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt:1
written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt:1
written_2/travel_guides/berlitz2/Vallarta-History.txt:0
written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:1
written_2/travel_guides/berlitz2/Bahamas-Intro.txt:0
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt:1
written_2/travel_guides/berlitz1/WhereToIndia.txt:1
written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt:1
written_2/travel_guides/berlitz2/China-History.txt:0
written_2/travel_guides/berlitz2/Costa-WhatToDo.txt:0
written_2/travel_guides/berlitz2/CostaBlanca-History.txt:0
written_2/travel_guides/berlitz2/Nepal-WhatToDo.txt:0
written_2/travel_guides/berlitz2/NewOrleans-History.txt:0
written_2/travel_guides/berlitz2/Paris-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Paris-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Poland-History.txt:0
written_2/travel_guides/berlitz2/Poland-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Portugal-History.txt:0
...

```

## What "grep -r -c "Coconut" is doing & why is it useful?"

## Lets break down the command:

* What exactly does "grep -r -c "Coconut"" do? 
* As we mentioned earlier, "grep" is a command used to search through files containing text for a specific "pattern", in this instance the pattern was "Coconut". 
* We are also utilizing the "-r" option which allows grep to search recursively through the directories and subdirectories of the current directory.
* Finally, we use the "-c" command option that counts the number times the specified pattern is found in the files contained in the directories.


# Here is another example using "grep -c"

## Example 2: "grep -r -w -o "surfing" *.txt | sort | uniq -c | sort -nr"

```

pwd

/c/Users/Chance/Desktop/CSE15L/LabReport3/skill-demo1-data-main/skill-demo1-data-main/written_2/travel_guides

cd berlitz2

grep -r -w -o "surfing" *txt | sort | uniq -c | sort -nr

      3 Vallarta-WhatToDo.txt:surfing
      3 PuertoRico-WhereToGo.txt:surfing
      3 California-WhatToDo.txt:surfing
      2 Portugal-WhereToGo.txt:surfing
      2 Bali-WhereToGo.txt:surfing
      2 Bahamas-WhatToDo.txt:surfing
      1 Vallarta-WhereToGo.txt:surfing
      1 PuertoRico-WhatToDo.txt:surfing
      1 CstaBlanca-WhereToGo.txt:surfing
      1 CostaBlanca-WhatToDo.txt:surfing
      1 CanaryIslands-WhatToDo.txt:surfing
          
      
```

## What "grep -r -w -o "surfing" *.txt | sort | uniq -c | sort -nr" is doing & why is it useful?"

## Lets break down the command:

* What exactly does "grep -r -w -o **"surfing"** *.txt | sort | uniq -c | sort -nr" do? 
* As we mentioned earlier, "grep" is a command used to search through files containing text for a specific "pattern", in this instance the pattern was **"surfing"**. 
* We are also utilizing the "-r" option which allows grep to search recursively through the directories and subdirectories of the current directory.
* We then apply the "-w" command to search for the exact string "surfing" and not any strings that contain "surfing" such as "windsurfing".
* We then utilize the "-o" command option that outputs the specified matching string found withing the file, in this case it is **"surfing"**.
* We then apply "*.txt | sort" command specifications. First "*.txt" declares that grep will only search through files containing ".txt" extenstions, Second "| sort" sorts the results obtained from the previous command.
* Lastly, we apply the "| uniq -c | sort -nr" commands. The "| uniq -c" removes any duplicate lines and "-c" specifcally displays how many times "surfing" appears in each file. Finally, "| sort -nr" is applied. The command sorts the output in numerical descending order, with the file containing the most occurences "surfing" at the top.



## Why is it useful?

* If you're a fan of coconuts and want to vacation in a place most likely to have them, it would be very beneficial to use the "grep -r -c "Coconut"" command to search through all the "travel_guides" located in "written_2" and find the ones that contain "Coconut" most often in their text. This is the easiest way to ensure that your next vacation is likely to contain coconuts!
* Or maybe you have a love for surfing and want to find out what destination is all about getting their surf on! If thats the case the using "grep -r -w -o **"surfing"** *txt | sort | uniq -c | sort -nr" will present you with the perfect list of destinations that will be perfect for those looking for a great surf destination.


    ..✨ <img src="https://user-images.githubusercontent.com/122570751/218375731-1d908d28-b74a-4d1a-bac6-eeb1b2b2a92e.png" width=10% height=10%> ✨..









________________________________________________________________________________________________________________________________________________________

## Alternative Method 2: **"-e"**



## **grep -e**
* The "-e" command allows you to use grep to search for multple "patterns" at the same time.
* After succesfully navgiating to the correct directory, you could type "grep -l -r -e "Pattern1" -e "Pattern2" to search rercusively through the directories and subdirectories of the current directory and print out files that contain either "Pattern1", "Pattern2" or both.

# Here are 2 different examples of utilizing "grep -e":

## Example 1: "grep -l -r -e "Mountains" -e "Rivers""

```
pwd

/c/Users/Chance/Desktop/CSE15L/LabReport3/skill-demo1-data-main/skill-demo1-data-main

grep -l -r -e "Mountains" -e "Rivers"

written_2/non-fiction/OUP/Berk/ch1.txt
written_2/non-fiction/OUP/Castro/chA.txt
written_2/travel_guides/berlitz1/HandRJamaica.txt
written_2/travel_guides/berlitz1/IntroDublin.txt
written_2/travel_guides/berlitz1/WhatToIsrael.txt
written_2/travel_guides/berlitz1/WhatToJamaica.txt
written_2/travel_guides/berlitz1/WhatToLosAngeles.txt
written_2/travel_guides/berlitz1/WhereToDublin.txt
written_2/travel_guides/berlitz1/WhereToItaly.txt
written_2/travel_guides/berlitz1/WhereToJapan.txt
written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt
written_2/travel_guides/berlitz1/WhereToLosAngeles.txt
written_2/travel_guides/berlitz1/WhereToMalaysia.txt
written_2/travel_guides/berlitz2/Bali-WhereToGo.txt
written_2/travel_guides/berlitz2/Beijing-WhereToGo.txt
written_2/travel_guides/berlitz2/Budapest-History.txt
written_2/travel_guides/berlitz2/Budapest-WhereoGo.txt
written_2/travel_guides/berlitz2/California-History.txt
written_2/travel_guides/berlitz2/California-WhereToGo.txt
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt
written_2/travel_guides/berlitz2/China-WhereToGo.txt
written_2/travel_guides/berlitz2/Costa-History.txt
written_2/travel_guides/berlitz2/Costa-WhereToGo.txt
written_2/travel_guides/berlitz2/Crete-WhereToGo.txt
written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
written_2/travel_guides/berlitz2/Vallarta-History.txt
written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt

```
## What "grep -l -r -e "Mountains" -e "Rivers"" is doing & why is it useful?"

## Lets break down the command:

* What exactly does "grep -l -r -e "Mountains" -e "Rivers"" do? 
* As we mentioned earlier, "grep" is a command used to search through files containing text for a specific "pattern", in this instance the patterns are "Mountains" and "Rivers". 
* We are also utilizing the "-l","-r" command options which allows grep to search recursively through the directories and subdirectories of the current directory and lists the names of the files that contain the specified "patterns".
* Finally, we utilize the **"-e"** command option that allows us to search for multiple "patterns" at the same time. In this instance we are searching for either "Mountains" or "Rivers" or files that contains both.

# Here is another example using "grep -e"

## Example 2: "grep -r -w -o "surfing" *.txt | sort | uniq -c | sort -nr"

```

pwd

/c/Users/Chance/Desktop/CSE15L/LabReport3/skill-demo1-data-main/skill-demo1-data-main/written_2/travel_guides

cd berlitz2

grep -r -w -o "surfing" *txt | sort | uniq -c | sort -nr

      3 Vallarta-WhatToDo.txt:surfing
      3 PuertoRico-WhereToGo.txt:surfing
      3 California-WhatToDo.txt:surfing
      2 Portugal-WhereToGo.txt:surfing
      2 Bali-WhereToGo.txt:surfing
      2 Bahamas-WhatToDo.txt:surfing
      1 Vallarta-WhereToGo.txt:surfing
      1 PuertoRico-WhatToDo.txt:surfing
      1 CstaBlanca-WhereToGo.txt:surfing
      1 CostaBlanca-WhatToDo.txt:surfing
      1 CanaryIslands-WhatToDo.txt:surfing
          
      
```

## What "grep -r -w -o "surfing" *.txt | sort | uniq -c | sort -nr" is doing & why is it useful?"

## Lets break down the command:

* What exactly does "grep -r -w -o **"surfing"** *.txt | sort | uniq -c | sort -nr" do? 
* As we mentioned earlier, "grep" is a command used to search through files containing text for a specific "pattern", in this instance the pattern was **"surfing"**. 
* We are also utilizing the "-r" option which allows grep to search recursively through the directories and subdirectories of the current directory.
* We then apply the "-w" command to search for the exact string "surfing" and not any strings that contain "surfing" such as "windsurfing".
* We then utilize the "-o" command option that outputs the specified matching string found withing the file, in this case it is **"surfing"**.
* We then apply "*.txt | sort" command specifications. First "*.txt" declares that grep will only search through files containing ".txt" extenstions, Second "| sort" sorts the results obtained from the previous command.
* Lastly, we apply the "| uniq -c | sort -nr" commands. The "| uniq -c" removes any duplicate lines and "-c" specifcally displays how many times "surfing" appears in each file. Finally, "| sort -nr" is applied. The command sorts the output in numerical descending order, with the file containing the most occurences "surfing" at the top.



## Why is it useful?

* If you're a fan of coconuts and want to vacation in a place most likely to have them, it would be very beneficial to use the "grep -r -c "Coconut"" command to search through all the "travel_guides" located in "written_2" and find the ones that contain "Coconut" most often in their text. This is the easiest way to ensure that your next vacation is likely to contain coconuts!
* Or maybe you have a love for surfing and want to find out what destination is all about getting their surf on! If thats the case the using "grep -r -w -o **"surfing"** *txt | sort | uniq -c | sort -nr" will present you with the perfect list of destinations that will be perfect for those looking for a great surf destination.


    ..✨ <img src="https://user-images.githubusercontent.com/122570751/218375731-1d908d28-b74a-4d1a-bac6-eeb1b2b2a92e.png" width=10% height=10%> ✨..
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
