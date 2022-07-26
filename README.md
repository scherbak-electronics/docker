# Docker how to

## Change php.ini and nginx config in docker using kubernetes lens IDE

Navigate to Workloads > Pods in the main menu: 

<img src="images/pic1.jpg" width="500">
<br>
<br>
<br>

Find your php-fpm pod where you want to change php.ini, 
in my case it's `php-fpm import` and open it:

<img src="images/pic2.jpg" width="500">
<br>
<br>
<br>

Scroll down to the Volumes section and click on link to it's config map:

<img src="images/pic3.jpg" width="500">
<br>
<br>
<br>

It will open php.ini so you can edit it like this:


<img src="images/pic4.jpg" width="500">
<br>
<br>
<br>

After make changes in php.ini scroll down and save it by clicking save button below:

<img src="images/pic6.jpg" width="500">
<br>
<br>
<br>

Then navigate to Deployments, select `php-fpm` and restart it to apply php.ini changes:

<img src="images/pic7.jpg" width="500">
<br>
<br>
<br>

After container restarted verify that changes updated.
Navigate back to the Pods and select `php-fpm` pod, then scroll down to Mounts section and copy path to php.ini file (path inside the container):

<img src="images/pic5.jpg" width="500">
<br>
<br>
<br>

Then click terminal button at the top blue bar and put the following here:
```
$ nano /usr/local/etc/php/php.ini
```
open the php.ini with `nano` at the folder you just copied from Mounts section.
All changes you have done should be here now.