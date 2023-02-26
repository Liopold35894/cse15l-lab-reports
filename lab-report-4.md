# **Steps for coding competition**
For this lab, I am reproducing the steps for the competition.

Step 1 to 3: Set up the repository needed for the competition.

Step 4: Log into ieng6
Keys pressed: `<up><up><up><enter>`
Description: The `ssh cs15lwi23abj@ieng6.ucsd.edu` command was 3 up in the search history, so I use the arrow to acess it, and press enter to log into the ieng6.
  
![alt text](https://github.com/Liopold35894/cse15l-lab-reports/blob/main/step%204%20-%20login%20to%20ieng6.png?raw=true)

Step 5: Clone your fork of the repository from your Github account
Keys pressed: `<up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><enter>`
Description: The `git clone git@github.com:Liopold35894/lab7.git`command was 16 up in the search history,  I accessed it using the arrow key and proceeded to clone the repository by pressing enter.

![alt text](https://github.com/Liopold35894/cse15l-lab-reports/blob/main/step%205%20-%20Clone%20fork%20repository.png?raw=true)
  
Step 6: Run the tests, demonstrating that they fail
Keys pressed: `cd l<tab><enter> <up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><enter> <up><up><up><up><up><up><up><up><up><up><up><up><up><up><enter>`
Description: The use `cd lab7/` command, tab to auto-complete lab7/, then enter. 19 up in the search history to access `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` 
and press enters to compile all java files in the current directory. Then 14 up in the search history to access `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples`
, press enter to run the test.
  
![alt text](https://github.com/Liopold35894/cse15l-lab-reports/blob/main/Step%206%20-%20Run%20the%20tests%2C%20demonstrating%20that%20they%20fail.png?raw=true)

Step 7: Edit the code file to fix the failing test
Keys pressed: `nano <shift>l<tab>java<enter> <down> <right><right><right><right><right><right><right><right><right><right><right><right> <backspace>2 <ctrl>o<enter> <ctrl>x`
Description: use `nano ListExample.java` to edit the file, shift to capitalize the letter l, tab to auto-complete, and then press enter to access the file. press down all the way until reach the correct row, then right to the letter we want to change. 
Backspace to delete 1 and change to 2 to fix the code, then ctrl-o and enter to save the change. Finally, ctrl-x to leave the file. 

![alt text](https://github.com/Liopold35894/cse15l-lab-reports/blob/main/Step%207%20-%20Edit%20the%20code%20file%20to%20fix%20the%20failing%20test.png?raw=true)
  
Step 8: Run the tests, demonstrating that they now succeed
Keys pressed: `<up><up><up><enter> <up><up><up><enter>`
Description: `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` command was 3 up in the search history, so I use the arrow to access it, and press enter to compile all java files in the current directory. 
I also use 3 up to access `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples` command, then presses enter to run the test. 

![alt text](https://github.com/Liopold35894/cse15l-lab-reports/blob/main/Step%208%20-%20Run%20the%20tests%2C%20demonstrating%20that%20they%20now%20succeed.png?raw=true)
  
Step 9: Commit and push the resulting change to your Github account
Keys pressed: `<up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><enter> <up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><enter>
<up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><enter>`
Description: `git add ListExamples.java` command was 21 up in the search history, so I use the arrow to access it, and pressed enter to add changes to the directory. Then I access `git commit ListExamples.java -m "Updated"` 
with another 21 up, and press enters to commit the changes with messages. Then I access `git push` with another 21 up, and press enters to push the changes back to my GitHub account.

![alt text](https://github.com/Liopold35894/cse15l-lab-reports/blob/main/Step%209%20-%20Commit%20and%20push%20the%20resulting%20change%20to%20your%20Github%20account.png?raw=true)

This is what I do during the competition to shorten the time and complete all the steps at the same time. 
