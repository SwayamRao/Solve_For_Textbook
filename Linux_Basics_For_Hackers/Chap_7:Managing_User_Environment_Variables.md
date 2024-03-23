# Managing_User_Environment_Variables

#### 1. View all of your environment variables with the `more` command.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ set | more
'!'=0
'#'=0
'$'=4078
'*'=(  )
-=3569JXghiks
0=/usr/bin/zsh
'?'=0
@=(  )
ARGC=0
CDPATH=''
COLORFGBG='15;0'
COLORTERM=truecolor
COLUMNS=157
COMMAND_NOT_FOUND_INSTALL_PROMPT=1
CPUTYPE=x86_64
DBUS_SESSION_BUS_ADDRESS='unix:path=/run/user/1000/bus'
DESKTOP_SESSION=lightdm-xsession
DISPLAY=:0.0
DOTNET_CLI_TELEMETRY_OPTOUT=1
EGID=1000
--snip--
}
````

---


#### 2. Use the `echo` command to view the `HOSTNAME` variable.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ host=`hostname`
                                                                                                                                                             
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ echo "$host"    
GRIMLOCK
````

---


#### 3. Find a method to change the slash (`/`) to a backslash ('\') in the faux Microsoft `cmd PS1` example (see Listing 7.2).

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ PS1='C:\\'
````

---


#### 4. Create a variable names `MYNEWVARIABLE` and put your name in it.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ MYNEWVARIABLE=grimlock

````

---


#### 5. Use `echo` to view the contents of `MYNEWVARIABLE`.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ echo "$MYNEWVARIABLE" 

grimlock
````

---


#### 6. Export `MYNEWVARIABLE` so that it's available in all environments.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ export MYNEWVARIABLE
````

---


#### 7. Use the echo command to view the contents of the `PATH` variable.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ echo $PATH           
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/games:/usr/games
````

---


#### 8. Add your home directory to the `PATH` variable so that any binaries in your home directory can be used in any directory.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ PATH=$PATH:/home/kali

````

---


#### 9. Change your `PS1` variable to "World's Greatest Hacker:".

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ PS1="World's Greatest HAcker"
                                                                                                                                                             
World's Greatest HAcker

````

---