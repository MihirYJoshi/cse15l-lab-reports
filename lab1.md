The First Step is to Install VS Code:
To install VS Code, one must first go to their website and download the correct file for their computer. This is the link to the VS Code downloading website: [Visual Studio Code](https://code.visualstudio.com/). After going through the download button, one will see the screen with the different Operating Systems and their corresponding downloads. The image is shown below.
<img width="1080" alt="Screenshot 2023-01-25 at 1 23 41 PM" src="https://user-images.githubusercontent.com/43663025/214694104-6df92558-d57d-453d-a3ed-234575e7f275.png">

Once this is downloaded, open VS Code. Once it is open, one should see the following screen. This means that it is working and has been downloaded properly.
![img](https://user-images.githubusercontent.com/43663025/211922805-172fc8bb-2d2a-4fc5-b552-fd541ede7a2c.png)

To open the terminal in VS Code, simply drag the blue bar from the bottom of the screen or right-click on a file and click on "Open in Integrated Terminal" to start the terminal as shown below.
<div></div>
<img width="424" alt="Screenshot 2023-01-25 at 1 27 42 PM" src="https://user-images.githubusercontent.com/43663025/214694924-b7815ac3-1776-42ed-948c-2a3ff2fd20cc.png">

The Second Step is to Remotely Connect to the Server:
First ssh into the server with your account name. The name is `cs151wi23zz` with the zz replaced with ones personal code. Add @ieng6.ucsd.edu as that is the server that one would need to ssh into. One must type in yes if it is ones first time. Then enter the password assiciated with the account.

<img width="573" alt="Screenshot 2023-01-11 at 11 20 30 AM" src="https://user-images.githubusercontent.com/43663025/211921210-3f7ca91d-4263-41e2-806f-ab4123028d41.png">

The user will then logged in and was welcomed. Information on CPU usage and Cluster Status will also be displayed
<img width="735" alt="Screenshot 2023-01-11 at 11 25 52 AM" src="https://user-images.githubusercontent.com/43663025/211924120-66858875-37d0-4041-b51c-e76b03b54594.png">

In the image, a new folder called folder1 was created in the home where one can run terminal commands, run python, and print txt files. One should use  `pwd` to find the current directory and `cd` to change to the home directory. One can create a python file that prints hello world using `vi` and then use python to run the file. This would print out hello world. One can then use `rm` to remove the file and list the files out. One can then use `cd..` to return to the source folder and created a new hello world file outside the folder.

<img width="514" alt="Screenshot 2023-01-11 at 12 10 02 PM" src="https://user-images.githubusercontent.com/43663025/211921222-ce54ab67-ff25-4b8a-9cab-56c31608222f.png">

Once can then use `cd folder1` to change into folder1, remove the hello world file that was inside using `rm ` and move the hello world text file that was created into the folder from the home directory using `mv`. After returning to the home directory and printing the present working directory using `pwd`, one can print all the files on one's account (including hidden) using `ls-lat` and one's current files (without hidden) and info using `ls-ltr`. One can then use `-a` to print hidden files. `cat` can be used to print hello.txt

![Screenshot 2023-01-11 at 1 19 49 PM](https://user-images.githubusercontent.com/43663025/211921207-38039b0f-a226-4590-b022-02584b64c207.png)

One may use `cd ..` to exit the folder and run an `ls` command to list all the other computers that are on the server. However, others cannot connect to those servers because they may not have the permission to do so.

<img width="578" alt="Screenshot 2023-01-12 at 2 19 00 PM" src="https://user-images.githubusercontent.com/43663025/212193559-9b2b777b-85bc-418b-986b-a9889e23ab1d.png">

One can also copy hello.txt from the outside folder on to one's computer using `scp` and run a `cat` command to display the files' contents

<img width="563" alt="Screenshot 2023-01-12 at 2 16 21 PM" src="https://user-images.githubusercontent.com/43663025/212193667-8e49b2c0-213b-430e-aecf-7748c95bb022.png">


