# A container for your PHP applications


## run the container 
``
make run
``

## stop the container
``
make stop
``

## enter into container
``
make ssh-root
``

## You must place your application into the /www folder

## You need to create a vhost.
example:  
``
make ssh-root
make vhost APP=<the folder's name of your application>
``

## Edit the vhost file for error logs for an app different from symfony
example for Laravel:  
``
cd /etc/apache2/sites-available
``  

``
vim <your app>.conf
``  

``
ErrorLog /var/www/projects/<your app>/storage/logs/apache_error.log
``  

``
a2ensite <your-app>.conf
``  

``
service apache2 restart
``  

### Mail RoundCube Fix Problem if it happens
``
service dovecot restart
``

