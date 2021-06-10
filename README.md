# TASK
## 1. Create a volume using  AWS EBS and attach to your ubuntu instance and mount it to /root/welcome
<img src="ebs.png"> 
```
$sudo -i
#root-fdisk /dev/xvdf
n        //for new partition
enter    //partition type
enter    // 1-4 (no)
enter    // first sector
+500M // last sector 
p        // for printing the created partition
w      // save 
#root- mkfs.xfs  /dev/xvdf
#root-mkdir /root/welcome
#root- mount  /dev/xvdf1/root/welcome
#root- df-hT 
```

## 2. Create a index.html in that having "HII LNB" written in that in mounted location
```
root#- echo  " " >tp.html
root#- vim tp.html
// Hello LNB
:wq!  
```

## 3. Volume detach and attach to new machine in which apache is installed and apache root directory should be /root/new
```
$ sudo -i
root#- apt install apache2
root#-systemctl status apache2
root#-mkdir /root/new
root#- cd /var/www
root#-ls
root#-cd html/
root#-ls
root#-cd /etc/apache2/sites-available
root#-ls
root#-vim 000-defualt.conf
// change the document root  to /root/new
//wq! 
root#-systemctl restart apache2
```
  
