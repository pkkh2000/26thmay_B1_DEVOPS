# TASK 

## 1. Create a  ALB that redirects 70% traffic to taregt 1 and 30% traffic to target 2.
ALB -> Listeners -> view/edit rules -> target 1- 70
                                    -> target 2-30
<img src=alb.png>                                 
                                    

## 2. In target 1 and 2 install apache2 web server
```
$ sudo -i
root#- apt install apache2
root#-systemctl status apache2 

$ sudo -i
root#- apt install apache2>
root#-systemctl status apache2 
```

## 3. Target 1 web server should display message in its output.
```
root#- echo  " " >idk.html
$ sudo -i
root#- vim idk.html>
// Hello My name is Khan && I am not a terriost
:wq! 
```

## 4. Target 2 web server should display message in its output.
```
root#- echo  " " >idk.html
$ sudo -i
root#- vim idk.html
// Welcome to Hogwards
:wq!
```
