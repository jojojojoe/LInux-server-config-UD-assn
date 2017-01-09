This is an simple example to set up a server which can serve web app. 

## Set up your server

#### General configuration

- After you logged in you remote server, the first thing is to disable the root access `PermitRootLogin no`, then `sudo adduser username` create new user and git it sudoer access.
- To make your server more secure, configur a firewall is very import, your can use the toole called "ufw" to allow and deny some ports and applications. This is an example to allow ssh and chage its port to 2200:


	```
	sudo ufw default deny incomint
	sudo ufw default allow outgoing
	sudo allow ssh
	sudo allow 2200/tcp
	```
- To login more securely, use RSA keys instead of passwords.

#### Install third-party resources

- Install what dependencies your application depend on.
	- The general resources like Git, ntp, pip.
	- Then install the web app dependencies, such as wsgi, oauth2client, httplib2, requests, redis, sqlalchemy.

#### Ip address

- ip: 35.167.109.149
- ssh port: 2200
- Web app URL: 35.167.109.149
