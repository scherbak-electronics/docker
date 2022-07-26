# Docker how to

## Change php.ini and nginx config in docker using kubernetes lens IDE

Navigate to Workloads > Pods in the main menu: 
![pic1](images/pic1.jpg)

Find your php-fpm pod where you want to change php.ini, in my case it's `php-fpm import` and open it:
![pic2](images/pic2.jpg)

Scroll down to the Volumes section and click on link to it's config map:
![pic3](images/pic3.jpg)

