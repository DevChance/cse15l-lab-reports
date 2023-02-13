# **✨ Welcome to my Lab Report #3 ✨** 

Written by: Chance Spurlin

------------------------------------

# First, we will be looking into the "grep" command & 4 alternative command-line options that utilize **"grep"**



## What is **"grep"** & how can it be applied?



- **"grep"** is a command used to search through files containing text for a specific "pattern". It will then print out the lines that contain the specified "pattern" that was found in the text that was located in the designated directory.



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
* Finally, we use the "-c" command option that counts the number times the specified pattern is found in the files contained in the directories and displays the number of occurences.


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
* We then utilize the "-o" command option that outputs the specified matching string found within the file, in this case it is **"surfing"**.
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

## Example 2: "grep -n -e "Aztec" Vallarta-History.txt"

```

pwd

/c/Users/Chance/Desktop/CSE15L/LabReport3/skill-demo1-data-main/skill-demo1-data-main/written_2/travel_guides

cd berlitz2

pwd

/c/Users/Chance/Desktop/CSE15L/LabReport3/skill-demo1-data-main/skill-demo1-data-main/written_2/travel_guides/berlitz2

grep -n -e "Aztec" Vallarta-History.txt 

7:The region’s history has some marked differences from the history of Mexico as a country. Although artifacts show that both the Aztec and Olmec pre-Hispanic cultures had a presence in the area, ancient civilizations created no notable settlements here. This fact, coupled with the geography of the region, spared it much of the bloodshed and turmoil of the Spanish conquest. With the imposing Sierra Madre Occidental mountain range running the length of the Pacific coastline, isolating it from the rest of mainland Mexico, the Pacific coast was able to develop at a slower, more tranquil pace.
10:Puerto Vallarta was launched into the international spotlight when Hollywood director John Huston decided to film the Tennessee Williams’ play, Night of the Iguana, on nearby Mismaloya Beach. Its history, however, runs much deeper than that event. Recent archeological findings show six different cultures lived in the area, with settlements dating back to 300 b.c. The most important was part of the kingdom of Xalisco, centered in the modern state of Nayarit. A marked Aztec influence is also present, probably due to the centuries-long migration of Aztecs from the legendary city of Aztlán, on the Pacific coast, to Tenochtitlan, present-day Mexico City. Remains of these cultures can be seen in the Museo del Río Cuale.    
27:In the early 1500s, Aztecs conquered the province of Coyuca, located between present-day Zihuatanejo and the Coyuca lagoon, and established a coastal capital, which they called Zihuatlan, “Place of Women,” named for the local matriarchal society. Residents today claim that the place was named for the beauty of the women, and means, “place of beautiful women.” 
...
      
```

## What "grep -n -e "Aztec" Vallarta-History.txt" is doing & why is it useful?"

## Lets break down the command:

* What exactly does "grep -n -e "Aztec" Vallarta-History.txt" do? 
* As we mentioned earlier, "grep" is a command used to search through files containing text for a specific "pattern", in this instance the pattern was **"Aztec"**. 
* We are also utilizing the "-n" option which causes grep to display the specific line number that the "Aztec" was found in.
* Lastly, we apply the "-e" command to search for all the occurrences of the string "Aztec" "in Vallarta-History.txt".
* We then specify the directory destiniation, which in this case is "Vallarta-History.txt" because we are looking into this destination specifically.



## Why is it useful?

* Using "-e" with the "grep" command is very useful for the user to search for multiple strings or "patterns" through the specified directory.
* You caan implement multiple "-e" to continously add "patterns" that you intend to search for using "grep".
* In the first example, we can see how it could be beneficial to search for both "Mountains" and "Rivers" simultaneously utilizing the "-e" command so that we can find a destination that contains either "Mountains", "Rivers" or both. That way we can ensure we vacation in a terrain that we enjoy!
* In the second example, we utilize "-e" to specify that we are searching for instances of "Aztec" within the ".txt" file. 
* We also apply "-n" which displays the line number that contains the specified "pattern" or in this case "Aztec".
* This would be useful if we wanted to look further into a specific topic. In this instance we wanted to learn more about "Aztec" history in Vallarta, Mexico.

________________________________________________________________________________________________________________________________________________________


## Alternative Method 3: **"--color"**



## **grep --color**
* The "--color" command is used to highlight the specified "pattern". 
* In our example we use "Aztec" to highlight the keyword "Aztec" in a specified ".txt" file.
* This allows the user to easily identifiy the specified "pattern" from the text.

# Here are 2 different examples of utilizing "grep --color":

## Example 1: "grep --color -n -e "Aztec" Vallarta-History.txt"

```

pwd

/c/Users/Chance/Desktop/CSE15L/LabReport3/skill-demo1-data-main/skill-demo1-data-main/written_2/travel_guides

cd berlitz2

pwd

/c/Users/Chance/Desktop/CSE15L/LabReport3/skill-demo1-data-main/skill-demo1-data-main/written_2/travel_guides/berlitz2

grep --color -n -e "Aztec" Vallarta-History.txt

7:The region’s history has some marked differences from the history of Mexico as a country. Although artifacts show that both the <p> <span style="color: red">Aztec</span> </p> and Olmec pre-Hispanic cultures had a presence in the area, ancient civilizations created no notable settlements here. This fact, coupled with the geography of the region, spared it much of the bloodshed and turmoil of the Spanish conquest. With the imposing Sierra Madre Occidental mountain range running the length of the Pacific coastline, isolating it from the rest of mainland Mexico, the Pacific coast was able to develop at a slower, more tranquil pace.
10:Puerto Vallarta was launched into the international spotlight when Hollywood director John Huston decided to film the Tennessee Williams’ play, Night of the Iguana, on nearby Mismaloya Beach. Its history, however, runs much deeper than that event. Recent archeological findings show six different cultures lived in the area, with settlements dating back to 300 b.c. The most important was part of the kingdom of Xalisco, centered in the modern state of Nayarit. A marked Aztec influence is also present, probably due to the centuries-long migration of Aztecs from the legendary city of Aztlán, on the Pacific coast, to Tenochtitlan, present-day Mexico City. Remains of these cultures can be seen in the Museo del Río Cuale.    
27:In the early 1500s, Aztecs conquered the province of Coyuca, located between present-day Zihuatanejo and the Coyuca lagoon, and established a coastal capital, which they called Zihuatlan, “Place of Women,” named for the local matriarchal society. Residents today claim that the place was named for the beauty of the women, and means, “place of beautiful women.” 
38:Even though Puerto Escondido is the more mature tourist destination of the two, Huatulco has the deepest historical roots. The Aztecs and Chichimecs (a Nahuatl-speaking warrior community) knew Huatulco as an important trading port long before the arrival of the Spanish conquistadors.     
...

```
# As seen from my Visual Studio Code Terminal:

![image](https://user-images.githubusercontent.com/122570751/218576865-ac464b59-10fb-4f1c-a627-de1a17b00540.png)

## So what exactly does "grep --color -n -e "Aztec" Vallarta-History.txt" do & why is it useful?"

## Lets break down the command:

* What exactly does "grep --color -n -e "Aztec" Vallarta-History.txt" do? 
* As we mentioned earlier, "grep" is a command used to search through files containing text for a specific "pattern", in this instance the pattern was "Aztec". 
* We are also utilizing the "--color" command option which causes any instance of "Aztec" to be highlighted in the designated color so that it is easily identifiable.
* Then, we implement the "-n", and "-e" command options to display the line number where the matching "pattern" is found. "-e" is then used to specify that we are searching for "Aztec" in this scenario.
* Finally, we specify the directory. As you can see, we have selected "Vallarta-History.txt" as the file we planned to navigate.


# Here is another example using "grep --color"

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
* We then utilize the "-o" command option that outputs the specified matching string found within the file, in this case it is **"surfing"**.
* We then apply "*.txt | sort" command specifications. First "*.txt" declares that grep will only search through files containing ".txt" extenstions, Second "| sort" sorts the results obtained from the previous command.
* Lastly, we apply the "| uniq -c | sort -nr" commands. The "| uniq -c" removes any duplicate lines and "-c" specifcally displays how many times "surfing" appears in each file. Finally, "| sort -nr" is applied. The command sorts the output in numerical descending order, with the file containing the most occurences "surfing" at the top.



## Why is it useful?

* If you're a fan of coconuts and want to vacation in a place most likely to have them, it would be very beneficial to use the "grep -r -c "Coconut"" command to search through all the "travel_guides" located in "written_2" and find the ones that contain "Coconut" most often in their text. This is the easiest way to ensure that your next vacation is likely to contain coconuts!
* Or maybe you have a love for surfing and want to find out what destination is all about getting their surf on! If thats the case the using "grep -r -w -o **"surfing"** *txt | sort | uniq -c | sort -nr" will present you with the perfect list of destinations that will be perfect for those looking for a great surf destination.


    ..✨ <img src="https://user-images.githubusercontent.com/122570751/218375731-1d908d28-b74a-4d1a-bac6-eeb1b2b2a92e.png" width=10% height=10%> ✨..





 
> **Great Job! Check out these additional commands you can try.**
>    - cd
>    - ls -lat
>    - cd ~
>    Any idea what they do?
  
## You finished! Great Job!
