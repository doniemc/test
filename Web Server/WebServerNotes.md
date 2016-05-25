<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Web Server Notes](#web-server-notes)
	- [Connect to Server Via SSH](#connect-to-server-via-ssh)
	- [Drupal Setup](#drupal-setup)

<!-- /TOC -->

# Web Server Notes

## Connect to Server Via SSH

On windows use Putty.exe

On Linux Open Terminal and use SSH command

```bash
ssh exs535imwyxr6-dev@ssh.eu.platform.sh
```
Navigate to the following folder
```bash
cd /etc/apache2/sites-available
```
Copy the default file
```bash
sudo cp default-ssl.conf NewSiteName.conf
```
Edit New Conf file
```bash
sudo nano NewSiteName.conf
```
![alt Sky](assets/WebServerNotes-4437f.png "apache2")

Use the up/down arrows to navigate through the document

Change the DoucmentRoot to point at the root of the website.

*Note the use of forward slashes.*

Exit nano:
```bash
Ctrl-x
```

You will be prompted to save

If you are using a port other than the default Port 80 it will have to be added to the ports.conf file

Navigate to the following folder
```bash
cd /etc/apache2
```
Edit ports.conf file
```bash
sudo nano ports.conf
```
Add new line for the port required under Listen 80:
```bash
Listen 80
Listen 8080
```
Use the a2ensite tool to enable each of our sites like this:
```bash
sudo a2ensite MyNewSite.conf
```

Restart Apache to make these changes take effect:
```bash
sudo service apache2 restart
```

More information is availble here:

https://www.digitalocean.com/community/tutorials/how-to-set-up-apache-virtual-hosts-on-ubuntu-14-04-lts

##Drupal Setup
