
##  commands
yum -y update
yum install java-1.8.0-openjdk
java -version


## java alternatives
update-alternatives --config java


## create variable JAVA_HOME
export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.212.b04-0.el7_6.x86_64/jre/bin/java


## Fontes
	https://www.liquidweb.com/kb/install-java-8-on-centos-7/
	https://www.digitalocean.com/community/tutorials/how-to-install-java-on-centos-and-fedora