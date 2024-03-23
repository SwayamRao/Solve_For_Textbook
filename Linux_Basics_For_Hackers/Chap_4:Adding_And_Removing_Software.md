# Adding And Removing Software

#### 1. Install a new software package from the Kali repository.

---

````shell
┌──(root㉿GRIMLOCK)-[/home/grimlock/Bash]
└─# apt-cache search snort                
fwsnort - Snort-to-iptables rule translator
golang-github-jasonish-go-idsrules-dev - Go IDS rule parser
ippl - IP protocols logger
libdaq-dev - Data Acquisition library for packet I/O - development files
libdaq2 - Data Acquisition library for packet I/O - shared library
libdaq3 - Data Acquisition library for packet I/O - shared library
libdaq3-dev - Data Acquisition library for packet I/O - development files
oinkmaster - Snort rules manager
psad - Port Scan Attack Detector
sagan-rules - Real-time System & Event Log Monitoring System [rules]
snort - flexible Network Intrusion Detection System
snort-common - flexible Network Intrusion Detection System - common files
snort-common-libraries - flexible Network Intrusion Detection System - libraries
snort-common-libraries-dbgsym - debug symbols for snort-common-libraries
snort-dbgsym - debug symbols for snort
snort-doc - flexible Network Intrusion Detection System - documentation
snort-rules-default - flexible Network Intrusion Detection System - ruleset
suricata - Next Generation Intrusion Detection and Prevention Tool
                                                                                                                                                             
┌──(root㉿GRIMLOCK)-[/home/grimlock/Bash]
└─# apt-get install snort 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  cython3 libadwaita-1-0 libatk-adaptor libbabeltrace1 libboost-dev libboost1.74-dev libc6-dbg libcodec2-1.1 libdav1d6 libjavascriptcoregtk-4.0-18
  libopenblas-dev libopenblas-pthread-dev libopenblas0 libplacebo292 libpython3-all-dev libsource-highlight-common libsource-highlight4v5 libucl1 libvpx7
  libwebkit2gtk-4.0-37 libxsimd-dev python3-all-dev python3-backcall python3-beniget python3-gast python3-pickleshare python3-pyatspi python3-pythran
  python3-requests-toolbelt zenity zenity-common
Use 'sudo apt autoremove' to remove them.
The following additional packages will be installed:
  libdaq3 libestr0 libfastjson4 liblognorm5 oinkmaster rsyslog snort-common snort-common-libraries snort-rules-default
Suggested packages:
  rsyslog-mysql | rsyslog-pgsql rsyslog-mongodb rsyslog-doc rsyslog-openssl | rsyslog-gnutls rsyslog-gssapi rsyslog-relp snort-doc
The following NEW packages will be installed:
  libdaq3 libestr0 libfastjson4 liblognorm5 oinkmaster rsyslog snort snort-common snort-common-libraries snort-rules-default
0 upgraded, 10 newly installed, 0 to remove and 137 not upgraded.
Need to get 3650 kB of archives.
After this operation, 15.7 MB of additional disk space will be used.
Do you want to continue? [Y/n] Y
Get:1 http://kali.download/kali kali-rolling/main amd64 snort-common-libraries amd64 3.1.82.0-0kali1 [269 kB]                       
Get:4 http://kali.download/kali kali-rolling/main amd64 libestr0 amd64 0.1.11-1 [9204 B]                                                                    
Get:6 http://kali.download/kali kali-rolling/main amd64 liblognorm5 amd64 2.0.6-4 [67.2 kB]                                 
Get:5 http://mirror.aktkn.sg/kali kali-rolling/main amd64 libfastjson4 amd64 1.2304.0-1 [28.9 kB]                                
Get:7 http://kali.download/kali kali-rolling/main amd64 rsyslog amd64 8.2402.0-1 [728 kB]                                                      
Get:3 http://mirror.kku.ac.th/kali kali-rolling/main amd64 snort-common all 3.1.82.0-0kali1 [117 kB]
Get:10 http://kali.download/kali kali-rolling/main amd64 oinkmaster all 2.0-4.2 [80.3 kB]                                                                   
Get:8 http://mirror.kku.ac.th/kali kali-rolling/main amd64 libdaq3 amd64 3.0.12-0kali3 [36.0 kB]    
````

---


#### 2. Remove that same software package.

---

````shell
┌──(root㉿GRIMLOCK)-[/home/grimlock/Bash]
└─# apt-get remove snort 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  cython3 libadwaita-1-0 libatk-adaptor libbabeltrace1 libboost-dev libboost1.74-dev libc6-dbg libcodec2-1.1 libdaq3 libdav1d6 libestr0 libfastjson4
  libjavascriptcoregtk-4.0-18 liblognorm5 libopenblas-dev libopenblas-pthread-dev libopenblas0 libplacebo292 libpython3-all-dev libsource-highlight-common
  libsource-highlight4v5 libucl1 libvpx7 libwebkit2gtk-4.0-37 libxsimd-dev oinkmaster python3-all-dev python3-backcall python3-beniget python3-gast
  python3-pickleshare python3-pyatspi python3-pythran python3-requests-toolbelt rsyslog snort-common snort-common-libraries snort-rules-default zenity
  zenity-common
Use 'sudo apt autoremove' to remove them.
The following packages will be REMOVED:
  snort
0 upgraded, 0 newly installed, 1 to remove and 137 not upgraded.
After this operation, 9681 kB disk space will be freed.
Do you want to continue? [Y/n] Y
(Reading database ... 424281 files and directories currently installed.)
Removing snort (3.1.82.0-0kali1) ...
Processing triggers for man-db (2.12.0-3) ...
Processing triggers for kali-menu (2023.4.7) ...
                                                 
````

---


#### 3. Update your repository.

---

````shell
Get:1 https://packages.microsoft.com/repos/vscode stable InRelease [3594 B]
Hit:2 https://packages.microsoft.com/repos/code stable InRelease       
Err:1 https://packages.microsoft.com/repos/vscode stable InRelease
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY EB3E94ADBE1229CF
Hit:3 http://http.kali.org/kali kali-rolling InRelease
Reading package lists... Done
W: GPG error: https://packages.microsoft.com/repos/vscode stable InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY EB3E94ADBE1229CF
E: The repository 'https://packages.microsoft.com/repos/vscode stable InRelease' is not signed.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.

````

---


#### 4. Upgrade your software packages.

---

````shell
┌──(root㉿GRIMLOCK)-[/home/grimlock/Bash]
└─# apt-get upgrade
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Calculating upgrade... Done
The following packages were automatically installed and are no longer required:
  cython3 libadwaita-1-0 libatk-adaptor libbabeltrace1 libboost-dev libboost1.74-dev libc6-dbg libcodec2-1.1 libdaq3 libdav1d6 libestr0 libfastjson4
  libjavascriptcoregtk-4.0-18 liblognorm5 libopenblas-dev libopenblas-pthread-dev libopenblas0 libplacebo292 libpython3-all-dev libsource-highlight-common
  libsource-highlight4v5 libucl1 libvpx7 libwebkit2gtk-4.0-37 libxsimd-dev oinkmaster python3-all-dev python3-backcall python3-beniget python3-gast
  python3-pickleshare python3-pyatspi python3-pythran python3-requests-toolbelt rsyslog snort-common snort-common-libraries snort-rules-default zenity
  zenity-common
````

---


#### 5. Select a new piece of software from github and clone it to your system.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ git clone git clone https://github.com/GHubgenius/slowloris.pl
````

---