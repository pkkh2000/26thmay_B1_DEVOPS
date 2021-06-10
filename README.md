# TASK 1
## To block your machine ip to ssh server and acccess from your ssh server from your mobile using juice ssh
```
$ iptables -A INPUT -s 192.168.43.215 -j DROP
 for mobile in termux 
$ssh harrypotter@192.168.43.215
```
# TASK 2
## to chnage the port number for ssh and then ssh to that machine using new port no
```
$sudo vim /etc/ssh/sshd_config
```
## Remove and Change port number from line 
```
$systemctl restart sshd.service 
$ssh -p 23 harrypotter@192.168.43.215
```
