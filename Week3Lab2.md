# ✨ Welcome to my Lab Report #2 ✨ 
Written by: Chance Spurlin
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
* In the handleRequest method it takes the parameter "URI url" and when given a relevant argument such as a url with "/add-message" the int num is incremented by one to keep track of the number of messages.
* If the url has the argument "/add-message" the ".split" method uses "=" as an argument to split the string into a string array called "finalString". 
* Then using the ".join" method and also utilizing "\n" as the delimeter/argument so that a new line is produced each time a message is returned. The messages are then taken from "finalString" and copied into ArrayList "allMsg". The ArrayList "allMsg" contains all of the arguments that are passed through the URI url handle if "/add-message" is present.
## What Values of the Relevant Fields Change from These Specified Request:
* The values that change from the above requests are: **int num** (Keeps track of the number of "/add-message" requests), **String[] finalString** (Contains the final collection of strings), **String[] initialString** (Contains the first set of strings retrieved from the url provided, including "s"), **ArrayList allMsg** (Contains all messages previously added and returns them), and **URI url** (Contains the url address).


________________________________________________________________________________________________________________________________________________________


 
## Part 2: Bug & Fix

**Failure Inducing Input as JUnit Test:**

 As viewable below, two lists are created with the following contents
   > ## List 1: "H", "He", "Hel", "Hell", "Hello"
 
   > ## List 2: null, "Go", "Goo", "Good", "Good Bye". 
  
 In the JUnit test we check to see whether the merge method is working properly and returned a merged list that correctly combined List 1 and List 2 together in alphabetical order. But when we try to add a null to either list and merge the contents. The merge method is unable to handle the request due to the null contained in the list.
 
```
import static org.junit.Assert.*;
import java.util.ArrayList;
import java.util.List;
import org.junit.*;

public class Lab3ListTest {
    private List<String> vacantList1;
    private List<String> vacantList2;



@Before
public void setUp() throws Exception {
  vacantList1 = new ArrayList<>();
  vacantList2 = new ArrayList<>();
}

@Test 
public void testMergeTwoListsNull() {
   this.vacantList1.add("H");
   this.vacantList1.add("He");
   this.vacantList1.add("Hel");
   this.vacantList1.add("Hell");
   this.vacantList1.add("Hello");
   this.vacantList2.add(null); //Null causes a failure inducing input. The program was not originaly designed to merge lists will "null".
   this.vacantList2.add("Go");
   this.vacantList2.add("Goo"); 
   this.vacantList2.add("Good");
   this.vacantList2.add("Good Bye");
   assertArrayEquals(new String[]{"Go","Goo","Good","Good Bye","H","He","Hel","Hell","Hello"}, ListExamples.merge(vacantList1,vacantList2).toArray());  
} 
``` 
 
**Non-Failure Inducing Input as JUnit Test:**

As viewable below, in this example we have a NON-FAILURE inducing input.
Two lists are created with the following contents:
   > ## List 1: "H", "He", "Hel", "Hell", "Hello"
 
   > ## List 2: "G", "Go", "Goo", "Good", "Good Bye". 
 
In the JUnit test we check to see whether the merge method is working properly and returned a merged list that correctly combined List 1 and List 2 together in alphabetical order.
``` 
@Test 
public void testMergeTwoLists() {
   this.vacantList1.add("H");
   this.vacantList1.add("He");
   this.vacantList1.add("Hel");
   this.vacantList1.add("Hell");
   this.vacantList1.add("Hello");
   this.vacantList2.add("G");
   this.vacantList2.add("Go");
   this.vacantList2.add("Goo");
   this.vacantList2.add("Good");
   this.vacantList2.add("Good Bye");
   assertArrayEquals(new String[]{"G","Go","Goo","Good","Good Bye","H","He","Hel","Hell","Hello"}, ListExamples.merge(vacantList1,vacantList2).toArray());
}
```

 
## Output & Symptom

 
**The screenshot below is after running the two JUnit tests that are described above.**
- As you may notice, the first test attempts to merge two lists, one of which contains a null element. When the two lists are merged the "merge" method in ListExamples.java does not succesfully create a new alphabetical list containing the remaining elements so the test fails.
- While in the second test, the merge method is succesfully applied as the two lists are correctly merged into one list as shown by the "testMergeTwoLists()" JUnit test.

![image](https://user-images.githubusercontent.com/122570751/216841382-db3f7eee-9f3b-4d20-954c-9a689c283ef7.png)

 
 
## Bug Code: Before and After:

**Before:**
```
  static List<String> merge(List<String> list1, List<String> list2) {
    List<String> result = new ArrayList<>();
    int index1 = 0, index2 = 0;
    while(index1 < list1.size() && index2 < list2.size()) {
      if(list1.get(index1).compareTo(list2.get(index2)) < 0) {
      result.add(list1.get(index1));
      index1 += 1;
      }
      else {
        result.add(list2.get(index2));
        index2 += 1;
      }
    }
    while(index1 < list1.size()) {
      result.add(list1.get(index1));
      index1 += 1;
    }
    while(index2 < list2.size()) {
      result.add(list2.get(index2));
      index1 += 1;
    }
    return result;
  }
```
 
**After Fixed Code:**
```
  static List<String> merge(List<String> list1, List<String> list2) {
    List<String> result = new ArrayList<>();
    int index1 = 0, index2 = 0;
    while(index1 < list1.size() && index2 < list2.size()) {
      if(list1.get(index1) == null ){ //Checks to see if the first index of list1 contains a null, if it does index1 moves one spots.
        index1 += 1;
      }
      if(list2.get(index2) == null ){ //Checks to see if the first index of list2 contains a null, if it does index2 moves one spots.
        index2 += 1;
      }
      if(list1.get(index1).compareTo(list2.get(index2)) < 0) {
      result.add(list1.get(index1));
      index1 += 1;
      }
      else {
        result.add(list2.get(index2));
        index2 += 1;
      }
    }
    while(index1 < list1.size()) {
      result.add(list1.get(index1));
      index1 += 1;
    }
    while(index2 < list2.size()) {
      result.add(list2.get(index2));
      index1 += 1;
    }
    return result;
  }
```

As you can see above, in order to fix the code we have to check for a null in the specified index. If there is a null, the index is increased by one to move onto the next index position. This allows the list to continue copying the contents of the list onto the new list even if a null is found in either list.

                                
**Running JUnit again after bug fix:**

Nice! Now its passing **ALL** JUnit Tests!                             
                                
![image](https://user-images.githubusercontent.com/122570751/216842297-21e53ad2-1212-485c-a856-dce0f9689aa6.png)

                                
                                
                                
 ________________________________________________________________________________________________________________________________________________________

                                
                                

## Part 3: What I learned from the Labs

 - In the lab for week 2 I learned alot of new information pertaining to remote servers and how to write the code to create and run a server on ieng6 using java. Which I found to be very interesting and useful to learn.
 - In week 3 I learned about JUnit and how to write tests that can be used to check for bugs in your code. I really enjoyed learning about JUnit because it seems very applicable when trying to learn how to debug code. Learning how to write tests and understand JUnit more indepth is incredibly helpful and useful tool for software programmers. I hope to learn more about JUnit and how to implement it when coding.                                
                                
                                
________________________________________________________________________________________________________________________________________________________

