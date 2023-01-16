This blog post contains instructions on how to connect to the CSE basement and run commands in the terminal.

__Step 1__ : Looking up your CSE 15L account 
---
![Image](Screen Shot 2023-01-15 at 10.50.57 PM.png)
For this step, I went to the following link: [CSE 15L Password Lookup](https://sdacs.ucsd.edu/~icc/index.php)
Instead of opting to change my password to something else, I used my canvas log in password since it met the strength requirement. 



__Step 2__ : Installing VSCode
---
![Image](Screen Shot 2023-01-15 at 9.40.09 PM.png)
In order to login to your course-specific account using ieng6, you need to download VSCode and use the command line. For this particular step, I did 
not need to install the IDE since I had done that last quarter for CSE 11. If you don't have it installed, you can go to the [VSCode Website](https://code.visualstudio.com/download) and download the appropriate version (in my case, VSCode for Mac).

__Step 3__ : Opening the Terminal
---
![Image](Screen Shot 2023-01-15 at 10.58.11 PM.png)

Since I am using a Macbook, I did not need to install git for Windows nor did I need to download Git Bash.. However, to do so, you can go [here](https://gitforwindows.org/). To use bash for windows, you can follow the instructions on this [Stack Overflow page](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994). To remotely connect, first open a new terminal, which you can do by selecting "Terminal" -> "New Terminal" in the toolbar at the top of your screen. You can also click towards the bottom of the VSCode screen and drag up. On my computer, I opened the bash terminal by clicking the down arrow next to the plus sign towards the bottom of the screen and then selecting bash. 

__Step 4__ : Using ssh and Logging in
---
In order to log in to your account, type the words ssh, followed by your course specific account username, followed by ieng6@ucsd.edu. This should be done in the command line in you terminal and should look like this:

- ssh cs15lwi23--@ieng6.ucsd.edu, The two dashes should be replaced by the last two letters in your username that are unique to you

__Step 5__ : Messages/Passwords
---
![Image](Screen Shot 2023-01-15 at 11.06.26 PM.png)
If you are connecting to the server for the first time, then you will get a question about whether you want to continue connecting. Type yes in the terminal and press enter.You will then be asked to type in the password that corresponds to your course-specific account. When doing so, the characters you type won't show up in the terminal, but they are being entered. After typing your password and pressing enter, you are now ready to run commands using th ecommand line. This is what your terminal should look like after connecting:

![Image](Screen Shot 2023-01-15 at 11.00.59 PM.png)

__Step 6__ : Trying Some Commands
---
Here are some of the commands that you can use:
* cd ~
* cd
* ls -lat
* ls -a
* pwd
* mkdir
* cp (cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/)
* cat /home/linux/ieng6/cs15lwi23/public/hello.txt

Here is an image of what my terminal looked like after running some commands:
![Image](Screen Shot 2023-01-12 at 1.36.18 PM.png)

And you're done! through following these exact steps, you should've connected to the CSE Basement server, be able to log in, and run the commands.
