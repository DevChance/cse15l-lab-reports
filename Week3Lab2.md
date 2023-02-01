# ✨ Welcome to my Lab Report #2 ✨
------------------------------------

## Throughout this page we will review a program that I have written called "StringServer" 

# Lets Begin!

**Part 1: The Code**
- Using NumberServer.java as a template I was able to understand how the numbers were stored into a string array and then added up into a single integer.
- Using those ideas I was able to construct a StringServer that allows the user to "add-messages" to the webpage so that it can keep track of any message the user may want to leave.

## Here is the Code:

![image](https://user-images.githubusercontent.com/122570751/215914170-d740f614-835c-4637-92ca-9662be0ea56b.png)

## After using "/add-message?s=Hello":
 
![Hello](https://user-images.githubusercontent.com/122570751/215906527-2da9437d-7e6c-44f0-9385-a6c95a737c6a.png)

## After using "/add-message?s=<String>" multiple times:

![Okay the end](https://user-images.githubusercontent.com/122570751/215906535-37ecd164-3a5f-46c3-ae3a-2a83031f3b02.png)

## Methods Called:
* First, the handleRequest method is called, this method handles the url.
* Then the url is analyzed to see if the path contains "/add-message" if it does, then ".split" method is called with "=" as the delimeter, this seperates everything between the equals sign.
* Then finally, the ".add" and ".join" methods are used to add messages to the ArrayList "allMsg". Which is finally returned using "String.join".
## Relevant Arguments and Values of the Methods:
* In the handleRequest method it takes the parameter "URI url" and when given a relevant argument such as a url with "/add-message" the int num is increment by one to keep track of the number of messages.
* If the url has the argument "/add-message" the ".split" method uses "=" as an argument to split the string into a string array called "finalString". 
* Then using the ".join" method and also utilizing "\n" as the delimeter/argument so that a new line is produced each time a message is returned. The messages are then taken from "finalString" and copied into ArrayList "allMsg". The ArrayList "allMsg" contains all of the arguments that are passed through the URI url handle if "/add-message" is present.
## What Values of the relevant fields of the class change from these request:
* The values that change from the above requests are: **int num** (Keeps track of the number of "/add-message" requests), **String[] finalString** (Contains the final collection of strings), **String[] initialString** (Contains the first set of strings retrieved from the url provided, including "s"), **ArrayList allMsg** (Contains all messages previously added and returns them), and ****URI url** (Contains the url address).


________________________________________________________________________________________________________________________________________________________

**Part 2: Bug & Fix**


________________________________________________________________________________________________________________________________________________________


** Part 3: What I learned**
- Connecting remotely to the ieng6 servers
  * First download [git](https://gitforwindows.org/) using the standard installation settings. **(No need to change any settings during installation)**
  * After git is finished downloading, follow the step by step instructions from this **[link](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994)**.
  * (This will allow you to set Git Bash terminal as your default terminal)
  * Great job!
 
________________________________________________________________________________________________________________________________________________________

