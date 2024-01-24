# Analyzing And Managing Networks
So here we first understand about the commands like ifconfig, iwconfig then to change the ip address,broadcast address,netmask and mac address using ifconfig command. Now we will jump into the questions <br>
1. Use command : ifconfig <br>
  This is used to get all info on active network interface.<br>
2. Use command : ifconfig eth0 192.168.1.1<br>
  This is used to change the ip address to the new ip address 192.168.1.1 on interface eth0 which is ethernet interface.<br>
3. To change the hardware address use command : <br>
   ifconfig eth0 down<br>
   ifconfig etho hw ether `<mac address>`<br>
   ifconfig eth0 up<br>
Now your mac address is changed to your desired mac address
4. Use command : iwconfig<br>
To know which wireless interface is active 
5. First let's understand what DHCP is , it stands for Dynamic Host Configuration Protocol. It is a server which is a deamon and assigns ip address to all the system presnet in subnet mask.<br>
Now use following command to reset your ip address on DHCP-assigned server<br>
  dhclient `<interface>`<br>
6.  To get the nameserver use command : dig `<url of target>` ns <br>
    To get the mailserver use command : dig `<url of target>` mx <br>
7. To add google's DNS to your file : <br> First go to '/etc/resolv.conf' <br> Then add google's DNS which is 8.8.8.8 <br>Then save and exit.