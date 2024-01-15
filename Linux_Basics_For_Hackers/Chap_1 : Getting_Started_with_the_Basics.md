# Getting_Started_with_the_Basics
Solutions to the questions :<br>
Let's first understand some symbols. <br>

The tilde character ~ is a shorthand for your home directory. Instead of typing /home/username, you can type the tilde.<br>

$ next to the cursor indicates the type of shell you're running. The dollar sign indicates it is the Bourne Again Shell (bash), the default Linux shell.

1. To solve this question<br> 
    First go to the root(/) directory by using command cd ../..<br>
    You will get output like : (grimlock㉿GRIMLOCK)-[/]
    <br>Here my username is grimlock and you will be getting your own username.<br>
    Then you can use command cd(change directory) [directory_name] to move into that directory.<br>
    Now use pwd(present working directory) command to check which directory you are currently in.

2. Now there is concept of creating multiple user in kali so to check about the user there is command whoami.

3. There are a number of wordlists present in kali so as to do password cracking. We can get all those wordlists using command
locate wordlist

4. For this question use command cat > filename ,then to exit and return back to prompt use ctrl-D.

5. First we will make a directory with mkdir command followed by directory name ,then we will use touch command to create a new file ,then to copy the file in the root directory we will use sudo cp filename /root/newfile_name  Here using this command we not only are copying the file into /root directory and also we are renaming it in the process.

So this was the solution for the chapter1 of the textbook I hope it was helpful :)
 