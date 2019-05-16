
## Install Tomcat
	sudo yum install tomcat


## Add the following JAVA_OPTS line to the file. Feel free to change the Xmx and MaxPermSize values—these settings affect how much memory Tomcat will use:

	sudo vi /usr/share/tomcat/conf/tomcat.conf

	`JAVA_OPTS="-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -Xmx512m -XX:MaxPermSize=256m -XX:+UseConcMarkSweepGC"`


## Install Admin Packages
	sudo yum install tomcat-webapps tomcat-admin-webapps 


## Install Online Documentation (Optional)
	sudo yum install tomcat-docs-webapp tomcat-javadoc


## Configure Tomcat Web Management Interface
	sudo vi /usr/share/tomcat/conf/tomcat-users.xml

	<tomcat-users>
	    <user username="admin" password="password" roles="manager-gui,admin-gui"/>
	</tomcat-users>




## To put our changes into effect, restart the Tomcat service:
	sudo systemctl start tomcat

## If you started the service earlier for some reason, run the restart command instead:
	sudo systemctl restart tomcat

## If you want Tomcat to run every time the server is booted up, you will need to enable the service:
	sudo systemctl enable tomcat

## Access the Web Interface
	http://server_IP_address:8080

## Let's take a look at the Manager App, accessible via the link 
	http://server_IP_address:8080/manager/html

## Now let's take a look at the Host Manager
	http://server_IP_address:8080/host-manager/html


## FONTES:
	https://www.digitalocean.com/community/tutorials/how-to-install-apache-tomcat-7-on-centos-7-via-yum



