# **Remote Acess**
For this section, we will be connecting to the remote server through Visual Studio Code with the course specific acount.

In order to connect to the server, we have to get the Visual Studio Code first. You can get it using the this link:
[Visual Studio Download](https://code.visualstudio.com/). Follow the instructions to download and install it on your computer.
If you already have it installed, like me, then you can just open it up. It should be something looks similar to this:
![alt text](https://github.com/Liopold35894/cse15l-lab-reports/blob/main/VScode%20screenshot.png?raw=true)

But that's not all, to be able to connect to the server, you have to look up for the course-specific acount for CSE15L that is bounded
with your UCSD acount. Use this link: [Look up for CSE15L Acount](https://sdacs.ucsd.edu/~icc/index.php)

For help on resetting the password, watch the tutorial here: [Tutorial: resetting the password](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit)

Your acount should be something looks like this: `cs15lwi23zz@ieng6.ucsd.edu`
the `zz` should be replace by the special characters that is assigned to you only, keep the rest of the format same. 

After getting getting the acount and resetting the password, open up the terminal on VSCode (Ctrl or Command + `, or use the Terminal → New Terminal menu option).
Enter the command: 
```
ssh cs15lwi23zz@ieng6.ucsd.edu
```
Then, the terminal will ask you "Are you sure you want to continue connecting (yes/no/[fingerprint])?"
Just type in yes, and then it will ask you to enter the password. When you're typing in the password, you wouldn't be able to see it on the screen, so just
keep typing and hit enter after you're finish. 



