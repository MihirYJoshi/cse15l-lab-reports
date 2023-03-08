I first SSH into my ieng6 server. Since I had previously done this, I was able to use my arrow keys and click the up arrow 3 times for this to pop up. I then pressed enter to run the command. Since I changed the access to public, I was able to log in immediately.

Keys Pressed: <up><up><up><enter> History: ssh cs15lwi23aio@ieng6.ucsd.edu

Screenshot 2023-02-23 at 2 19 46 PM

Result:

Screenshot 2023-02-23 at 2 23 07 PM



I then went to GitHub and copied the line under the SSH tab.
Screenshot 2023-02-23 at 2 25 03 PM

I then pasted this line in the terminal along with git clone and pressed enter.

Keys Pressed: <Command+V> <Control+A> <Git Clone> <enter>

Screenshot 2023-02-23 at 2 27 40 PM

Result:

Screenshot 2023-02-23 at 2 28 20 PM



I then needed to Run the Tests on the Repo and show that they fail. To do this I had to navigate to the repo and run the tests.
Key Pressed: <ls><cd> "l" <tab><enter> Auto Filled: lab7

This gave me this line:

Screenshot 2023-02-23 at 2 36 22 PM

I then ran this command to compile all the .java files in the directory:

javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java

I then ran this command to run the JUNIT Tests for the Java Test file:

java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests

This led to a failure in JUNIT:

Screenshot 2023-02-23 at 2 51 55 PM

I needed to fix the code in order for the code to compile. To do this I needed to open the ListExamples.java file in a vi editor and fix the code error.

Key Pressed: <vi> "L" <tab> "." <tab><enter> Auto Filled: ListExamples.java

This resulted in this editor:

Screenshot 2023-02-23 at 2 54 15 PM

I then navigated to the error in the file, pressed "i" to insert and replaced index1 += 1 with index2 += 1 to ensure that it is incrementing the correct variable. I then pressed <escape> :wq to save and quit the file.

I now needed to compile and run the tests on the new file. I was able to use the arrow keys to navigate through past commands and run the unit.

Kep Pressed: <up><up><up><up><up><enter> History: javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java

This ran this code which compiled:

Screenshot 2023-02-23 at 2 59 21 PM

To run the JUNIT Tests, I was able to use the arrow keys once again. This allowed the tests to run and pass:

Kep Pressed: <up><up><up><up><up><enter> History: java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests

Screenshot 2023-02-23 at 3 00 15 PM

Results:

Screenshot 2023-02-23 at 3 01 17 PM

I now needed to add and commit the new files and changes that I made. The code I entered was: git add --all which added the files. I then entered git commit to commit them.

This opened this file where I clicked "i" entered a commit message: "Fixed the errores in the file"

Screenshot 2023-02-23 at 3 04 34 PM

I then pressed <escape> :wq to save and quit the file.

Screenshot 2023-02-23 at 3 05 12 PM

Then the files were commited to the GitHub
