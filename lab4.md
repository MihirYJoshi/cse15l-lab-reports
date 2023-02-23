
I first SSH into my ieng6 server. Since I had previously done this, I was able to use my arrow keys and click the up arrow 3 times for this to pop up. I then pressed enter to run the command. Since I changed the access to public, I was able to log in immediately. 

Keys Pressed: `<up><up><up><enter>`

<img width="402" alt="Screenshot 2023-02-23 at 2 19 46 PM" src="https://user-images.githubusercontent.com/43663025/221043571-6afb84af-15ef-46be-bdb3-6457b30a0c93.png">

Result:

<img width="483" alt="Screenshot 2023-02-23 at 2 23 07 PM" src="https://user-images.githubusercontent.com/43663025/221044139-d0e9cc64-37ca-4f0f-8090-f68f4e255020.png">

<br>
</br>
I then went to GitHub and copied the line under the SSH tab.

<img width="306" alt="Screenshot 2023-02-23 at 2 25 03 PM" src="https://user-images.githubusercontent.com/43663025/221044488-e1e5c051-5410-4291-88b5-49acce8dd7b0.png">

I then pasted this line in the terminal along with `git clone` and pressed enter.

Keys Pressed: `<Command+V> <Control+A> <Git Clone> <enter>`

<img width="552" alt="Screenshot 2023-02-23 at 2 27 40 PM" src="https://user-images.githubusercontent.com/43663025/221044958-9849dc05-f42d-4e33-83ac-f5527d603712.png">

Result:

<img width="711" alt="Screenshot 2023-02-23 at 2 28 20 PM" src="https://user-images.githubusercontent.com/43663025/221045066-e008b803-2656-4bef-8807-d71e1098625f.png">

<br>
</br>
I then needed to Run the Tests on the Repo and show that they fail. To do this I had to navigate to the repo and run the tests.

Key Pressed: `<ls><cd> "l" <tab><enter>`
This gave me this line:

<img width="299" alt="Screenshot 2023-02-23 at 2 36 22 PM" src="https://user-images.githubusercontent.com/43663025/221046285-dd67fdd1-4055-45aa-a07a-cde9ab56f118.png">

I then ran this command to compile all the .java files in the directory:

`javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`

I then ran this command to run the JUNIT Tests for the Java Test file:

`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`

This led to a failure in JUNIT:

<img width="594" alt="Screenshot 2023-02-23 at 2 51 55 PM" src="https://user-images.githubusercontent.com/43663025/221048765-814e47b2-dc78-47f4-9198-f62d4ce593f0.png">
