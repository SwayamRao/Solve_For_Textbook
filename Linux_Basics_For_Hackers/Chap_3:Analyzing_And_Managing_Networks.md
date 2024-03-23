# Analyzing And Managing Networks

#### 1. Find information on your active network interfaces.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ ifconfig                                                      
lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 172  bytes 12306 (12.0 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 172  bytes 12306 (12.0 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

wlan0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 20.20.6.21  netmask 255.255.192.0  broadcast 20.20.63.255
        inet6 fe80::6c7f:b049:2155:9b79  prefixlen 64  scopeid 0x20<link>
        ether 40:1c:83:d0:c0:19  txqueuelen 1000  (Ethernet)
        RX packets 137841  bytes 15791863 (15.0 MiB)
        RX errors 0  dropped 13  overruns 0  frame 0
        TX packets 5164  bytes 2069587 (1.9 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

````

---


#### 2. Change the IP address on `eth0` to `192.168.1.1`.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ ifconfig eth0 194.168.1.1/24                                                     
````

---


#### 3. Change your hardware address on `eth0`.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ ifconfig eth0 down  

┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ ifconfig eth0 hw ether 00:11:22:33:44:55  

┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ ifconfig eth0 up  

````

---


#### 4. Check whether you have any available wireless interfaces active.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ iwconfig                 
lo        no wireless extensions.

wlan0     IEEE 802.11  ESSID:"RITSTUDENTS"  
          Mode:Managed  Frequency:5.785 GHz  Access Point: **:**:**:**:**:**   
          Bit Rate=1 Mb/s   Tx-Power=22 dBm   
          Retry short limit:7   RTS thr:off   Fragment thr:off
          Power Management:on
          Link Quality=53/70  Signal level=-57 dBm  
          Rx invalid nwid:0  Rx invalid crypt:0  Rx invalid frag:0
          Tx excessive retries:0  Invalid misc:3591   Missed beacon:0

````

---


#### 5. Reset your IP address to a DHCP-assigned address.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ dhclient iwconfig


````

---


#### 6. Find the nameserver and email server of your favorite website.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ dig swayamrao.me ns

; <<>> DiG 9.19.21-1-Debian <<>> swayamrao.me ns
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 56865
;; flags: qr rd ra; QUERY: 1, ANSWER: 2, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 512
;; QUESTION SECTION:
;swayamrao.me.                  IN      NS

;; ANSWER SECTION:
swayamrao.me.           1800    IN      NS      dns1.registrar-servers.com.
swayamrao.me.           1800    IN      NS      dns2.registrar-servers.com.

;; Query time: 240 msec
;; SERVER: 20.20.0.1#53(20.20.0.1) (UDP)
;; WHEN: Sat Mar 23 16:25:42 IST 2024
;; MSG SIZE  rcvd: 100

                                                                                                                                                             
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ dig swayamrao.me mx

; <<>> DiG 9.19.21-1-Debian <<>> swayamrao.me mx
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 52651
;; flags: qr rd ra; QUERY: 1, ANSWER: 5, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 512
;; QUESTION SECTION:
;swayamrao.me.                  IN      MX

;; ANSWER SECTION:
swayamrao.me.           1800    IN      MX      20 eforward5.registrar-servers.com.
swayamrao.me.           1800    IN      MX      15 eforward4.registrar-servers.com.
swayamrao.me.           1800    IN      MX      10 eforward1.registrar-servers.com.
swayamrao.me.           1800    IN      MX      10 eforward2.registrar-servers.com.
swayamrao.me.           1800    IN      MX      10 eforward3.registrar-servers.com.

;; Query time: 168 msec
;; SERVER: 20.20.0.1#53(20.20.0.1) (UDP)
;; WHEN: Sat Mar 23 16:25:45 IST 2024
;; MSG SIZE  rcvd: 192
````

---


#### 7. Add Google's DNS server to your `/etc/resolv.conf` file so your system refers to that server when it can't resolve a domain name query with your local DNS server.

---

````shell
┌──(grimlock㉿GRIMLOCK)-[~/Bash]
└─$ echo "nameserver 8.8.8.8" >> /etc/resolv.conf

````

---