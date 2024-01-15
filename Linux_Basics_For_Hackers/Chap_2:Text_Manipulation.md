# Text Manipulation
So we first solve the Hacker Challenge given in the textbook.<br>
To do that we first need to understand the command that the author used.<br>
Here I used my own file called chap2.txt.<br>

nl chap2.txt | tail -n+5<br>
The above command is used to print the data after the line 4 including the line 5. The nl is used to list numbers and we pipe it to tail command followed by -n+5.<br>

Similarly,  nl chap2.txt | head -n+5 <br>
It prints the lines starting from begining untill line 5 and it also include the line 5.

And nl chap2.txt | tail -n+5 | head -n 3<br>
This is used to get the first 3 lines from line 5.<br>

This was author's solution now lets jump to my solution<br>

nl chap2.txt | head -n 7 | tail -n+5 <br>
Here I first make it print lines so that it is easy to verify then I pipe it to head with -n 7 which means I need the first 7 lines then I again pipe it to tail with -n+5 which means I need the lines from 5 till the end which in this case is line 7.  

Now will solve the questions

1.  Use command : cd /usr/share/wordlists/metasploit    
     To get into the directory
2.  Use command cat passwords.lst          
   To get the contents of the file
3. Here use command : more passwords.lst             
  But yea ik its too long
4. Use command : less passwords.lst          
   To get the contents
5. Use command : nl passwords.lst
   Yea I got 88398 passwords but according to author it should be 88396 (ig it might be because I am refering to the edition released on 2018)
6. Use command nl passwords.lst | tail -n 20                          
   To get the last 20 passwords
7. Use command : cat password.lst | grep 123                      
    Here cat command first displays the passwords.lst then I piped it to grep to search for 123

These were the solutions for the question given in the textbook, I hope it helped you in some way or the other.
