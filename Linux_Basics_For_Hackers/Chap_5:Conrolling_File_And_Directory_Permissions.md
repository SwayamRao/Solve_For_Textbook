# Conrolling File And Directory Permissions
1. Command used for this is `ls -l` and we can notice the permissions on the file present in the directory.
2. There are two ways to change permissions using command `chmod`.<br>One is using decimal notation and another one is using UGO method <br> Command used for changing permissions using decimal notation `chmod 777 {filename}` Here 777 is used to give all permissions to all the users <br> Command used for changing permissions using UGO method is `chmod u+x {filename}` This command gives user executable permissions.
3. Use command `chown {Username} {File location}`
4. Use command `find / -user root -perm 2000` to get the files with the SGID bit. 

#### 1. Select a directory and run a long listing on it. Note the permissions on the files and directory.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ ls -l 
total 44
-rw-r--r-- 1 grimlock grimlock   53 Jan  2 13:36 brightness_high.sh
-rw-r--r-- 1 grimlock grimlock   55 Mar 23 15:57 brightness_low.sh
-rw-r--r-- 1 grimlock grimlock   14 Dec 20 13:51 csvtest.csv
-rw-r--r-- 1 grimlock grimlock   43 Dec 22 19:05 file123.txt
-rwxrwxrwx 1 grimlock grimlock  270 Dec 20 13:37 func.sh
-rw-r--r-- 1 grimlock grimlock  236 Dec 20 13:47 func1.sh
drwxr-xr-x 4 grimlock grimlock 4096 Jan 24 09:34 lab
-rwxrwxrwx 1 grimlock grimlock  120 Dec 19 19:18 login.sh
-rw-r--r-- 1 grimlock grimlock   82 Dec 22 19:05 sample.sh
-rw-r--r-- 1 grimlock grimlock   14 Dec 20 13:49 testfile1.txt
drwxr-xr-x 2 grimlock grimlock 4096 Jan 23 14:55 youtube
````

---


#### 2. Select a file you don't have permission to execute and give yourself execute permissions using the `chmod` command. Try using both the numerical method (`777`) and the UGO method.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ ls -l wow
-rw-r--r-- 1 grimlock grimlock 0 Mar 23 16:04 wow
                                                                                                                                                             
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ chmod 777 wow
                                                                                                                                                             
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ ls -l wow
-rwxrwxrwx 1 grimlock grimlock 0 Mar 23 16:04 wow

````

---


#### 3. Choose another file and change its ownership using `chown`.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ ls -l wow     
-rwxrwxrwx 1 grimlock grimlock 0 Mar 23 16:04 wow
                                                                                                                                                             
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ sudo su             
[sudo] password for grimlock: 
Sorry, try again.
[sudo] password for grimlock: 
┌──(root㉿GRIMLOCK)-[/home/grimlock/Bash]
└─# chown root wow  
                                                                                                                                                             
┌──(root㉿GRIMLOCK)-[/home/grimlock/Bash]
└─# ls -l wow
-rwxrwxrwx 1 root grimlock 0 Mar 23 16:04 wow

````

---


#### 4. Use the `find` command to find all files with the `SGID` bit set.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ find / -perm 2000                                 
find: ‘/usr/lib/mysql/plugin/auth_pam_tool_dir’: Permission denied
find: ‘/run/lightdm’: Permission denied
find: ‘/run/user/1000/systemd/inaccessible/dir’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/run/openvpn-server’: Permission denied
find: ‘/run/openvpn-client’: Permission denied
find: ‘/run/exim4’: Permission denied
find: ‘/run/cryptsetup’: Permission denied
find: ‘/run/systemd/propagate/colord.service’: Permission denied
find: ‘/run/systemd/propagate/upower.service’: Permission denied
find: ‘/run/systemd/propagate/rtkit-daemon.service’: Permission denied
````

---