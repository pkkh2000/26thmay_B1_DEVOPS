# TASK 1  
## 1.Create a directory new at location /mnt
```
$ sudo - mkdir /mnt/new
```
## 2. Create a volume using  AWS EBS and attach to your ubuntu instance.
<img src="ebs.png">

## 3.Create a partition and mount it on /mnt/new
```
$sudo fdisk /dev/xvdf
n        //for new partition
enter    //partition type
enter    // 1-4 (no)
enter    // first sector
+500M // last sector 
p        // for printing the created partition
w      // save 
$sudo mkfs.xfs  /dev/xvdf
$sudo mount  /dev/xvdf1/mnt/new
$sudo df-hT 
```
## 4.Install apache web server
$ sudo apt install apache2
$ sudo systemctl status apache2

## 5.Change apache web serevr root directory path  /var/www/html  to /mnt/new
```
root#- cd /var/www
root#-ls
root#-cd html/
root#-ls
root#-cd /etc/apache2/sites-available
root#-ls
root#-vim 000-defualt.conf
// change the document root  to /mnt/new
//wq! - to save
root#-systemctl restart apache2
```
