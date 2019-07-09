# Linux Server Configuration 

### General Information 
IP Address of the application instance: 13.235.155.183
URL of the application instance: http://ec2-13-235-155-183.ap-south-1.compute.amazonaws.com/
SSH port for accessing the server: 2200

### Software Packages Installed 
- finger 
- apache2 
- libapache2-mod-wsgi	
- ntp 
- postgresql 
- git 
- sqlalchemy 
- flask 
- flask-sqlalchemy 
- python-psycopg2 
- oauth2 

### Configuration Changes 
- Updated all the packages to their most recent versions, expcept one which couldn't be updated since the updated version contained amendments which could hamper the running of the current system. 
- Created a new superuser: 'grader'. 
- Generated a key-pair so that 'grader' could securely login to the syste via SSH. 
- Blocked all incoming SSH requests on port 22, rather made 2200 the operational one using uncomplicated firewall. 
- Blocked all inbound communications with the exception of HTTP, SSH, and NTP. 
- Allowed all outbound communications. 
- Disabled password login for any user by enforcing key-based login, and disabled remote login for 'root'. 
- Configured the local timezone to UTC. 
- Installed and configured Apache and mod_wsgi. 
- Installed and configured Postgresql. 
- Created a new database user: 'itemcatalog' and made a database 'itemcatalog' owned by 'itemcatalog'. 
- Installed Git, and cloned my 'item-catalog' repository on the server. 
- Made a few amendments to the source code in order for the application to work properly in the production environment. 
- Implemented third-party authentication using OAuth. 

### External References Used 
- https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps 
- https://www.digitalocean.com/community/tutorials/how-to-set-up-apache-virtual-hosts-on-ubuntu-14-04-lts 
- https://github.com/elnobun/Linux-Server-Configuration 
- https://github.com/harushimo/linux-server-configuration 
- https://github.com/ghoshabhi/P5-Linux-Config 