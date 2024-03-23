# Process_Management

#### 1. Run the `ps` command with the `aux` options on your system and note which process is first and which is last.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~]
└─$ ps aux             
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.0  22392 12616 ?        Ss   15:22   0:00 /sbin/init splash
root           2  0.0  0.0      0     0 ?        S    15:22   0:00 [kthreadd]
root           3  0.0  0.0      0     0 ?        I<   15:22   0:00 [rcu_gp]
root           4  0.0  0.0      0     0 ?        I<   15:22   0:00 [rcu_par_gp]
root           5  0.0  0.0      0     0 ?        I<   15:22   0:00 [slub_flushwq]
root           6  0.0  0.0      0     0 ?        I<   15:22   0:00 [netns]
root           8  0.0  0.0      0     0 ?        I<   15:22   0:00 [kworker/0:0H-events_highpri]
root          11  0.0  0.0      0     0 ?        I<   15:22   0:00 [mm_percpu_wq]
root          12  0.0  0.0      0     0 ?        I    15:22   0:00 [rcu_tasks_kthread]
root          13  0.0  0.0      0     0 ?        I    15:22   0:00 [rcu_tasks_rude_kthread]
root          14  0.0  0.0      0     0 ?        I    15:22   0:00 [rcu_tasks_trace_kthread]
root          15  0.0  0.0      0     0 ?        S    15:22   0:00 [ksoftirqd/0]
root          16  0.0  0.0      0     0 ?        I    15:22   0:01 [rcu_preempt]
root          17  0.0  0.0      0     0 ?        S    15:22   0:00 [migration/0]
root          18  0.0  0.0      0     0 ?        S    15:22   0:00 [idle_inject/0]
root          19  0.0  0.0      0     0 ?        S    15:22   0:00 [cpuhp/0]
root          20  0.0  0.0      0     0 ?        S    15:22   0:00 [cpuhp/1]
root          21  0.0  0.0      0     0 ?        S    15:22   0:00 [idle_inject/1]
root          22  0.0  0.0      0     0 ?        S    15:22   0:00 [migration/1]
root          23  0.0  0.0      0     0 ?        S    15:22   0:00 [ksoftirqd/1]

````

---


#### 2. Run the `top` command and note the two processes using the greatest amount of your resources.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ top
top - 15:57:38 up 35 min,  1 user,  load average: 0.47, 0.51, 0.44
Tasks: 245 total,   1 running, 244 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.4 us,  0.3 sy,  0.0 ni, 99.2 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st 
MiB Mem :  15755.9 total,  11517.9 free,   3246.5 used,   1912.2 buff/cache     
MiB Swap:    977.0 total,    977.0 free,      0.0 used.  12509.4 avail Mem 

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND                                                                               
    843 root      20   0 1797496 131744  72280 S   2.7   0.8   1:25.45 Xorg                                                                                  
  18871 grimlock  20   0  981556 114532  92452 S   2.3   0.7   0:02.18 qterminal                                                                             
   1166 grimlock  20   0 1195020 108264  78512 S   0.7   0.7   0:18.86 xfwm4                                                                                 
     16 root      20   0       0      0      0 I   0.3   0.0   0:01.80 rcu_preempt                                                                           
   1235 grimlock  20   0  333860  92820  19072 S   0.3   0.6   0:06.13 panel-13-cpugra                                                                       
   1237 grimlock  20   0  490168  27756  20724 S   0.3   0.2   0:05.77 panel-15-genmon 
````

---


#### 3. Use the `kill` command to kill the process that uses the most resources.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ kill 18871
````

---


#### 4. Use the `renice` command to reduce the priority of a running process to `+19`.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ renice 19 10902
10902 (process ID) old priority 0, new priority 19
````

---


#### 5. Create a script called `myscanning` (to see how to write a bash script, see Chapter 8; the content of the script is not important) with a text editor and then schedule it to run next Wednesday at `1 AM`.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ at 1:00am 09/09/2020
warning: commands will be executed using /bin/sh
at> /home/grimlock/timepass
at> <EOT>
job 1 at Wed Sep  9 01:00:00 2020
````

---