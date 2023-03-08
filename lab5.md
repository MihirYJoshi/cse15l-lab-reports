I would be able to run everything instantly by running all the tasks from lab 4 in a bash script.


In Lab 4, I started with ssh-ing onto the ieng6 server. To do this, I would type in the command:
  
    ssh cs15lwi23aio@ieng6.ucsd.edu


To create a bash script, I would first run this command in the terminal: `vi script.sh`

In Lab 4, I then went to GitHub and copied the line under the SSH tab. I will do the same here to put into the script. I will first put git clone in front to be able to clone the repository:

    git clone git@github.com:ucsd-cse15l-w23/lab7.git
    
This gives me this:

![Screenshot 2023-03-07 at 9 50 00 PM](https://user-images.githubusercontent.com/43663025/223630172-bddd4f26-c3f1-43f5-9bca-3dc2f176d548.png)

<br>
</br>
I then needed to Run the Tests on the Repo and show that they fail. To do this I had to navigate to the repo and run the tests. To do this in the script I typed in: 

    cd lab7
    
I then needed to compile all the .java files in the directory, so I added this to the script:

    javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java

I then added this command to run the JUNIT Tests for the Java Test file:

    java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests

These two commands compile the files and run the JUNIT tests. This led to a failure in JUNIT:

<img width="594" alt="Screenshot 2023-02-23 at 2 51 55 PM" src="https://user-images.githubusercontent.com/43663025/221048765-814e47b2-dc78-47f4-9198-f62d4ce593f0.png">

I needed to fix the code in order for the code to compile. To do this I needed to open the ListExamples.java file and fix the code error. For the code to work properly, I need to replace the last instance of `index1 += 1` with `index2 += 1`. To do this, I need to run a command that replaces the 3rd instance in a file. To do this, I used a sed command:

    sed -i '' '0,/index1 += 1/{/index1 += 1/{n;/index1 += 1/{s/index1 += 1/index2 += 1/;}}}' ListExamples.java
    
I then needed to compile all the .java files in the directory, so I added this to the script:

    javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java

I then added this command to run the JUNIT Tests for the Java Test file:

    java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests

These two commands compile the files and run the JUNIT tests. This led to both tests passing JUNIT:

![Screenshot 2023-03-07 at 10 22 29 PM](https://user-images.githubusercontent.com/43663025/223635174-9dd372b3-ba66-492b-8d06-50ea9321bc44.png)

I now needed to add and commit the new files and changes that I made. The line I needed to enter in the bash script to add and commit the files were: 

    git add --all
    
    git commit -m "commit"

Then the files were commited to the GitHub
