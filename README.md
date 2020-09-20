###############################################
## Generic files to be copied after
## installing tomcat on a server 
## Tomcat latest have issues that 
## you cannot start using right after installing
## 1. Copy contents of webapps.dist dir into webapps dir
## 2. Have to modify "context.xml" file to allow
## 	http conections from other than localhost
## 3. Have to include roles and users in "tomcat-users.xml"
#################################################
## This repo contains these 2 files.
## The users roles && passwords are :
## role rolename="manager-gui"/>
 <role rolename="manager-script"/>
 <role rolename="manager-jmx"/>
 <role rolename="manager-status"/>
 <user username="admin" password="admin" roles="manager-gui, manager-script, manager-jmx, manager-status"/>
 <user username="deployer" password="deployer" roles="manager-script"/>
 <user username="tomcat" password="s3cret" roles="manager-gui"/>

