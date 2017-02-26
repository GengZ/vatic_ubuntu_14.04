# vatic_ubuntu_14.04_installation_guide
with bug solution for ubuntu 14.04 offline usage

Basiclly follow the installation instruction of [original version](https://github.com/cvondrick/vatic/tree/contrib).

**Modifications required as below**

## INSTALL VATIC

1. replace the vatic-install.sh in **this** repo other than the **original one** and use it. 

## APACHE CONFIGURATION

1. edit /etc/apache2/sites-enabled/000-default.**conf**, the original version misses out the *.conf*...
2. this file should look like *000-default.conf* in this repo. (perhaps the only modifications for you, is the **DocumentRoot** and **WSGIScriptAlias**, change them to your local path as the **original repo** guiding. )

## SETUP

1. *conf.py* also got a sample in this repo, ( perhaps no changes need to be done...)

## OTHERS

1. some solutions for common **ERROR** is documented in *solutions.txt* in this repo. 
  *Note*:
  for the 3rd item in solutions.txt, it refers to the step where open the link after publishing. At that time, if you come across **SERVER  ERROR** on your screen when using the link given by *publishing*, check the /var/log/apache2/er\* file. If the content is identical with  the 3rd item, then try the solution :)

2. **ERROR** 

```
Could not reliably determine the server's fully qualified domain name, using 127.0.1.1.Set the 'ServerName' directive globally to suppress this message
```
 **SOLUTION:**
   Add **ServerName 127.0.0.1** in file: /etc/apache2/apache2.conf
   then run: sudo apache2ctl graceful
***  

Any issue is welcome :) 
