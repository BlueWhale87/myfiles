Command to install zeek

1. Install ethtool
2. Update your system 
	apt-get update
3. Upgrade your system 
	apt-get upgrade
4. Install zeek pre-req 
	sudo apt-get install cmake make gcc g++ flex bison libpcap-dev libssl-dev python2-dev swig zlib1g-dev
5. Add zeek repositories to local repo
	wget -nv https://download.opensuse.org/repositories/security:/zeek/xUbuntu_22.04/Release.key -O Release.key

6. Addkey 
	apt-key add -< Release.key
7. Update package to see if there's new repo
	apt-get update
8. Add repo
	sudo sh -c "echo 'deb http://download.opensuse.org/repositories/security:/zeek/xUbuntu_22.04/ /' > /etc/
	apt/sources.list.d/security:zeek.list"

9. Update to see if we have any new repo
	apt-get update
10. Install zeek 
	apt-get install zeek-lts
11. Zeek is now installed!
12. To verify if we have installed,
	ls /opt/
	cd /opt/
	ls the binary package install location should be in /opt/zeek
	
	cd zeek/
	ls
	cd bin/
	./zeek -h
	./zeekctl -h
13. Installation is verified!