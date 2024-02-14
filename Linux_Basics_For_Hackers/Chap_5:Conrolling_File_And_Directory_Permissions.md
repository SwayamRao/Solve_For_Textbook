# Conrolling File And Directory Permissions
1. Command used for this is `ls -l` and we can notice the permissions on the file present in the directory.
2. There are two ways to change permissions using command `chmod`.<br>One is using decimal notation and another one is using UGO method <br> Command used for changing permissions using decimal notation `chmod 777 {filename}` Here 777 is used to give all permissions to all the users <br> Command used for changing permissions using UGO method is `chmod u+x {filename}` This command gives user executable permissions.
3. Use command `chown {Username} {File location}`
4. Use command `find / -user root -perm 2000` to get the files with the SGID bit. 