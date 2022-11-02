How to run this project in local server(Xampp)
1. We must have xampp server. (installed)
2. Make new folder in htdocs, folder name “complaintBox”
3. Paste all file in Certificate folder (Path: - C:\xampp\htdocs\complaintBox)
4. start two function of xampp server
a) Apache
b) MySQL
import database file in phpMyAdmin, database file present in root folder
<!-- file content|| file Name: httpd-vhosts.conf -->
# Virtual Hosts
#
# Required modules: mod_log_config

# If you want to maintain multiple domains/hostnames on your
# machine you can setup VirtualHost containers for them. Most configurations
# use only name-based virtual hosts so the server doesn't need to worry about
# IP addresses. This is indicated by the asterisks in the directives below.
#
# Please see the documentation at 
# <URL:http://httpd.apache.org/docs/2.4/vhosts/>
# for further details before you try to setup virtual hosts.
#
# You may use the command line option '-S' to verify your virtual host
# configuration.

#
# Use name-based virtual hosting.
#
##NameVirtualHost *:80
#
# VirtualHost example:
# Almost any Apache directive may go into a VirtualHost container.
# The first VirtualHost section is used for all requests that do not
# match a ##ServerName or ##ServerAlias in any <VirtualHost> block.
#
##<VirtualHost *:80>
    ##ServerAdmin webmaster@dummy-host.example.com
    ##DocumentRoot "C:/xampp/htdocs/dummy-host.example.com"
    ##ServerName dummy-host.example.com
    ##ServerAlias www.dummy-host.example.com
    ##ErrorLog "logs/dummy-host.example.com-error.log"
    ##CustomLog "logs/dummy-host.example.com-access.log" common
##</VirtualHost>

##<VirtualHost *:80>
    ##ServerAdmin webmaster@dummy-host2.example.com
    ##DocumentRoot "C:/xampp/htdocs/dummy-host2.example.com"
    ##ServerName dummy-host2.example.com
    ##ErrorLog "logs/dummy-host2.example.com-error.log"
    ##CustomLog "logs/dummy-host2.example.com-access.log" common
##</VirtualHost>
<VirtualHost *:80>
    DocumentRoot "C:\xampp\htdocs\complaintBox"
    ServerName complaintbox.co.in
    ServerAlias www.complaintbox.co.in
    ErrorLog "logs/complaintbox.co.in-error.log"
    CustomLog "logs/complaintbox.co.in-access.log" common
</VirtualHost>
<VirtualHost *:80>
    DocumentRoot "C:\xampp\htdocs"
</VirtualHost>



<!-- file content end -->

5. a txt file attached in this mail, just paste this file on path C:\xampp\apache\conf\extra
6. if your xampp already started stop it, and start again
7.Now we are ready to run our portal just search in browser http://complaintbox.co.in
