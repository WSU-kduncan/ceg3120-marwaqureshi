Part 2

1)

~ vim etc/hosts, then type information such as hostname, ip address, user, filename. 
Example of ip address and hostname shown which was used in the yml file.
10.0.1.10 WebServer1
10.0.1.11 WebServer2

2)

~ In order to SSH in between the systems utilizing their private IPs, it is best to use the private IP address,private key which is called ceg3120-aws-vm.pem and the username which is ubuntu; when ssh-ing into proxy. This method will obviously be used to ssh into Webserver1 and Webserver2 by using the same method. ssh -i ceg3120-aws-vm.pem ubuntu@privateIP. Also, with .ssh/config done cooreclty, ssh webserver2 command will do the job and you wouldnt need to use the IP. 

3) 

~ Modified file: /etc/haproxy/haproxy.cfg
~ configured frontend and backend  
~ sudo systemctl restart haproxy
~ https://www.haproxy.com/blog/the-four-essential-sections-of-an-haproxy-configuration/

4)

~ index.html from /var/www/html done for both webservers.
~ default, none
~ /var/www/html. default for site content
~ sudo systemctl restart apache2

5)

[screenshots]


 
