# Process_Management
1. In this question we first use `ps aux` command to list out the processes running on the system for all users. Here we get `/sbin/init splash` as first process and `ps aux` as last process.
2. `top` command is used to get the greedist process running in the system. In my case its "Xorg".
3. Use command `kill {option among the 64 diffrenet kill signals} [PID of the process]` or we can even use `killall {option} [hypothetical name of the process]`
4. Use command `renice 19 [PID of the process]`. Increasing the 'nice' value can be done by any user unlike decresing the nice vale which only can be done by root user. <br> More negative the nice value -> More priority.
5. Use any editor to create the script, then use command `at 1:00am [Date in MM/DD/YYYY format]` then give the complete location of the script to schedule the job. <br>Here we are using `at` command to schedule the job.  