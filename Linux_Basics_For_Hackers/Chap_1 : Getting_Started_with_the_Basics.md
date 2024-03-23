# Getting_Started_with_the_Basics

### 1.
Use the `ls` command from the root (`/`) directory to explore the directory structure of Linux. Move to each of the directories with the `cd` command and run `pwd` to verify where you are in the directory structure.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ ls -l
total 64
drwxr-xr-x 4 grimlock grimlock 4096 Mar 23 16:04 Bash
drwxr-xr-x 2 grimlock grimlock 4096 Mar 20 15:31 CTF
drwxr-xr-x 8 grimlock grimlock 4096 Mar 20 16:36 Desktop
drwxr-xr-x 3 grimlock grimlock 4096 Dec 26 13:44 Documents
drwxr-xr-x 2 grimlock grimlock 4096 Mar 20 16:02 Downloads
drwxr-xr-x 2 grimlock grimlock 4096 Dec 30 12:00 Lab

````

---


### 2.
Use the `whoami` command to verify which user you are logged in as.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ whoami        
grimlock

````

---


### 3.
Use the `locate` command to find wordlists that can be used for password cracking.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ locate /wordlists
/etc/theHarvester/wordlists
/etc/theHarvester/wordlists/dns-big.txt
/etc/theHarvester/wordlists/dns-names.txt
/etc/theHarvester/wordlists/dorks.txt
/etc/theHarvester/wordlists/general
/etc/theHarvester/wordlists/names_small.txt
/etc/theHarvester/wordlists/general/common.txt
/usr/bin/wordlists
/usr/lib/python3/dist-packages/theHarvester/wordlists
/usr/lib/python3/dist-packages/theHarvester/data/wordlists
/usr/lib/python3/dist-packages/theHarvester/data/wordlists/dns-big.txt
/usr/lib/python3/dist-packages/theHarvester/data/wordlists/dns-names.txt
/usr/lib/python3/dist-packages/theHarvester/data/wordlists/dorks.txt
/usr/lib/python3/dist-packages/theHarvester/data/wordlists/general
/usr/lib/python3/dist-packages/theHarvester/data/wordlists/names_small.txt
/usr/lib/python3/dist-packages/theHarvester/data/wordlists/general/common.txt
/usr/share/wordlists
/usr/share/amass/wordlists
/usr/share/amass/wordlists/all.txt
/usr/share/amass/wordlists/bitquark_subdomains_top100K.txt
/usr/share/amass/wordlists/deepmagic.com_top500prefixes.txt
/usr/share/amass/wordlists/deepmagic.com_top50kprefixes.txt
/usr/share/amass/wordlists/fierce_hostlist.txt
/usr/share/amass/wordlists/jhaddix_all.txt

````

---


### 4.
Use the `cat` command to create a new file and then append to that file. Keep in mind that `>` redirects input to a file and `>>` appends to a file.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ cat > temp.txt  
This is > operation
^C
                                                                                                                                                             
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ cat >> temp.txt
This is >> operation
^C
                                                                                                                                                             
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ cat temp.txt
This is > operation
This is >> operation

````

---


### 5.
Create a new directory called `hackerdirectory` and create a new file that directory named `hackedfile`. Now copy that file to your `/root` directory and rename it `secretfile`.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ mkdir hackerdirectory
                                                                                                                                                             
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ touch hackerdirectory/hackedfile

┌──(grimlock㉿GRIMLOCK)-[~]
└─$ cp hackerdirectory/hackedfile /root/secretfile
````

---
 