# Text Manipulation
#### 1. Navigate to `/usr/share/metasploit-framework/data/wordlists`. This is a directory of multiple wordlists that can be used to brute force passwords in various password-protected devices using Metasploit, the most popular pentesting and hacking framework.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ cd /usr/share/metasploit-framework/data/wordlists
````

---


#### 2. Use the `cat` command to view the contents of the file `password.lst`.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[/usr/share/metasploit-framework/data/wordlists]
└─$ more password.lst
!@#$%
!@#$%^
!@#$%^&
!@#$%^&*
!boerbul
!boerseun
!gatvol
!hotnot
!kak
!koedoe
!likable
!poes
!pomp
!soutpiel
````

---

#### 3. Use the `more` command to display the file `password.lst`.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[/usr/share/metasploit-framework/data/wordlists]
└─$ more password.lst
!@#$%
!@#$%^
!@#$%^&
!@#$%^&*
!boerbul
!boerseun
!gatvol
!hotnot
!kak
!koedoe
!likable
!poes
!pomp
!soutpiel
.net
0
000000
00000000
0007
007
007007
0s
0th

--snip--
````

---


#### 4. Use the `less` command to view the file `password.lst`.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[/usr/share/metasploit-framework/data/wordlists]
└─$ less password.lst

--snip--
````

---


#### 5. Now use the `nl` command to place line numbers on the passwords in `password.lst`. There should be around `88,396` passwords.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[/usr/share/metasploit-framework/data/wordlists]
└─$ nl password.lst              
     1  !@#$%
     2  !@#$%^
     3  !@#$%^&
     4  !@#$%^&*
     5  !boerbul
     6  !boerseun
     7  !gatvol
     8  !hotnot
     9  !kak
    10  !koedoe
    11  !likable
    12  !poes
    13  !pomp
    14  !soutpiel
    15  .net
    16  0
    17  000000
    18  00000000
    19  0007
    20  007
    21  007007
    22  0s
    23  0th
    24  1
    25  10
    26  100
    27  1000
    28  1000s
    29  100s
    30  1022
    31  10s
    32  10sne1
    33  1111
    34  11111
    35  111111
    36  11111111

--snip--
    88398  vagrant
````

---


#### 6. Use the `tail` command to see the last `20` passwords in `password.lst`.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[/usr/share/metasploit-framework/data/wordlists]
└─$ tail -20 password.lst 
zxcvbnm
zydeco
zygote
zygotic
zymurgy
zyrtec
zyuganov
zzz
zürich
Ågar
Ångström
éclair
éclairs
éclat
élan
émigré
émigrés
épée
étude
vagrant

````

---


#### 7. Use the `cat` command to display `password.lst` and pipe it to find all the passwords that contain `123`.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[/usr/share/metasploit-framework/data/wordlists]
└─$ cat password.lst | grep 123                      
123
123123
123321
1234
12345
123456
1234567
12345678
123456789
1234567890
1234qwer
123abc
123go
123qwe
a12345
abc123
abcd123
abcd1234
aki123
asdf1234
chris123
happy123
hello123
help123
jkl123
red123
test123
xxx123
xyz123
zxc123

````

---