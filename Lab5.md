# Part 1, Debugging Scenario 

## Student: 
I am designing a function for CSE department's enrollment system. My function prompts student to verify if he/she is a Computer Science major. If so, they can enroll in CSE100. Else, they cant enroll in CSE 100. For some reason, when I type input "Computer Science major" and check if it is the same string as allowed major "Computer Science" -- it tells me that I cant enroll in CSE 100. I made sure that there is no typos and that I do == instead of = assigning operation in the if statement. Please help! 

## TA: 
I see that your code is mostly correct. However, you should review a use of ``` == ``` with objects. We know from the class that two strings have different adresses in the memory. What does it mean if we want to compare them? 

## Student: 
After reading java documentation on ```==```, I realized that it compares whether two strings are the same object. Even though ``` == ``` with string can sometimes work correctly, it can lead to unexpected behavior. After reading documentation on strings, I found a good method to compare the value placed in objects instead of comparing the objects themself. I will use ``` equals ``` method instead. 

## File and Directory Structure:
Two files: ``` Code.java ``` that has the code to check and ``` test.sh ``` script that compiles and runs the Code.java. 

### Contents of the files: 

### Commands to trigger the 


