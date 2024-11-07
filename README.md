**                     **Quize Game using C++****
In this program, you will writing a class which helps simulate multiple-choice trivia questions, accept the user's answers, and provide a full key and a score at the end.

Part 0: Documenting the Code and following Programming Standards 

When developing code, it's crucial to document how the program works and adhere to programming standards. Add the program header below, replacing its information with details relevant to the program. Additionally, make sure that you follow the style guidelines for the course when developing the program. (Modules -> Module 0 -> C++ Programming Standards and Practices).

Code Block 8.3.1: Program Header Template
/*********************************************************************
File name: example.cpp
Author: <Your Name Here>
Date: XX/XX/XXXX

Purpose:
   Description of the purpose of the program.
Command Parameters:
   -
Input:
   Description of the input to the program.
Results:
   Description of what the program produces.
Notes:
   Description of any special information regarding this program.
*********************************************************************/
Part 1: Creating a Makefile 

In this program, you'll be using multiple C++ files, and you'll need to create a Makefile to properly compile them. Your Makefile should:

Compile each source file separately into object files (*.o).
Link the object files together to create an executable.
Include a run command to execute the program.
Include a clean command to remove all object files (*.o).


Implement parts 2-12 in a separate file dedicated to questions (question.cpp).

Part 2: Creating the Default Constructor 

Implement the following prototype for the Question class:

Question();


This constructor should initialize a Question object with no values (i.e., use empty strings for the question stem and choices, and 'X' for the answer key).



Part 3: Creating the Parameterized Constructor 

Implement the following prototype for the Question class:

Question(string, string[], char);


This constructor should initialize a Question object using the provided parameters: a question stem, an array of possible answers, and the letter of the correct answer.



Part 4: Creating the Question Setter 

Implement the following prototype for the Question class:

void setQuestionStem(string);


This function should set the passed parameter as the new question stem.



Part 5: Creating the Question Getter 

Implement the following prototype for the Question class:

string getQuestionStem();


This function should return the current question stem.



Part 6: Creating the Choices Setter 

Implement the following prototype for the Question class:

void setChoices(string []);


This function should set the passed array as the new possible answer choices.



Part 7: Creating the Choices Getter 

Implement the following prototype for the Question class:

string getChoice(int);


This function should return the answer choice at the specified index.



Part 8: Creating the Key Setter 

Implement the following prototype for the Question class:

void setKey(char);


This function should set the correct answer key to the passed parameter.



Part 9: Creating the Key Getter 

Implement the following prototype for the Question class:

char getKey();


This function should return the current answer key.



Part 10: Reordering the Possible Answers 

Implement the following prototype for the Question class:

void reorder(int);


This function should reorder the possible answer choices based on one of the following methods:

Method 1: Swap choices A with B, and C with D.
Method 2: Swap choices A with C, and B with D.
Method 3: Swap choices A with D, and B with C.
Any other number: Print "Invalid method specified." and exit the function.
Additionally, the correct answer key should be updated to reflect the new positions of the choices.



Part 11: Asking the Question 

Implement the following prototype for the Question class:

string ask();


This function should generate a formatted string containing the question and possible answers. The output should display the answer choices with labels like so: A. <choice>, B. <choice>, etc. Return the string to be displayed.



Part 12: Using a Lifeline 

Implement the following prototype for the Question class:

string useLifeline(int);


This function should provide lifeline options for the quiz:

Method 1: Simulates the "50/50" option from Who Wants to Be a Millionaire. This should eliminate two incorrect answers, leaving one correct and one incorrect answer.
Method 2: Simulates the "Ask the Audience" option. In this case, provide a random answer, which may or may not be correct.
The function should return a string explaining the result of the lifeline, such as the remaining answer choices for 50/50 or the audience recommendation. If an invalid option is passed, return an empty string.



Note: Since there is a random component to the lifelines, please seed the function with srand(time(0)); This should let you get the exact same results as expected output.

Code Block 8.3.2: Sample Test Driver Program Execution
$ make run
./program2_test.out

Testing setters and getters
Question 1 Stem: Which gas is the Earth's atmosphere primarily composed of? 
Question 1 first choice: Oxygen
Question 1 last choice: Hydrogen
Question 1 correct answer: C


Testing constructor and ask function
Which country is home to the Kangaroo?
A. China
B. India
C. Mexico
D. Australia
correct answer: D


Testing reorder methods
Which country is home to the Kangaroo?
A. India
B. China
C. Australia
D. Mexico
correct answer: C
Which country is home to the Kangaroo?
A. Australia
B. Mexico
C. India
D. China
correct answer: A
Which country is home to the Kangaroo?
A. China
B. India
C. Mexico
D. Australia
correct answer: D

Testing constructor and lifeline functions function
What is the process by which plants make their own food using sunlight?
A. Photosynthesis
B. Respiration
C. Fermentation
D. Transpiration

50-50 Lifeline:
A. Photosynthesis
D. Transpiration

Ask the Audience Lifeline: The audience suggests option D. Transpiration
Feel free to modify the test driver to thoroughly test any functions you write. Once you have completed testing your class with the test driver, you will compile it using the grading driver.



There is an object file named program2_driver.o available on the IDE. This file is the driver that will be used for grading, and you will not be able to view its source code. Modify your Makefile to link your question.cpp class with this grading driver object file. Then, run your program using the updated Makefile and the new driver.



Below is an example of what your program should do when using the grading driver.

Code Block 8.3.3: Sample Grading Driver Program Execution
$ make grade
./program2.out
Enter filename: questions.txt
Enter number of questions (1-10): 3
Enter question Reorder method (1-3): 2

1. What do you use to measure an angle?
A. Ruler
B. T-Square
C. Compass
D. Protractor
Your answer (enter the letter or L for lifeline): D

2. The Great Sphinx has the head of a human and the body of a what?
A. Lion
B. Alligator
C. Camel
D. Eagle
Your answer (enter the letter or L for lifeline): L
1: 50-50
2: Ask the audience
Which lifeline would you like to use: 1

50-50 Lifeline:
A. Lion
D. Eagle

Your answer (enter the letter): A

3. What is the flat rubber disc used in a game of ice hockey?
A. Tile
B. Puck
C. Birdie
D. Dart
Your answer (enter the letter or L for lifeline): C

Answers: 
D A B 

You got 2 correct out of 3
Final Score: 150



**Check this project:-**

**How to run this code:
STEP_1: Open the terminal with file directory(all files must be prsent in the same folder)
STEP_2: Type "Make" in terminal which will compile the program
STEP_3: Type "Make run" in the terminal.
STEP_4: Provide the infromation as needed**
