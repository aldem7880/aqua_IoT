## aqua_IoT
    this is fork of IoT.me below.
    purpose is to make it work under ubuntu 16.4 LTS and latest nodejs + mongodb

# TODO:
	- setup vagrant
	- autoconfig with ansible
	- fix errors :
        https://github.com/aldem7880/aqua_IoT/issues/1

# Install node.js
```
curl --silent --location https://deb.nodesource.com/setup_8.x | sudo bash -
sudo apt-get install --yes nodejs git

$ node -v
v8.12.0

```
 
# Set locale and Install latest stable MongoDB
```

sudo su -
export LANGUAGE=en_US.UTF-8
export LANG=en_US.UTF-8
export LC_ALL=en_US.UTF-8
locale-gen en_US.UTF-8
dpkg-reconfigure locales


sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10
echo "deb http://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.0.list
sudo apt-get update
sudo apt-get install -y mongodb-org
```
 
# Install Express-generator
    the -g option is used so that the package is installed globally, 
    meaning that we can now use it from the command line

# Try express -h to see the options now available
```
sudo npm install express-generator -g

/usr/bin/express -> /usr/lib/node_modules/express-generator/bin/express-cli.js
+ express-generator@4.16.0
added 10 packages from 13 contributors in 2.133s
```
 
# Install Nodemon
```
sudo npm install nodemon -g
...
+ nodemon@1.18.5
added 233 packages from 136 contributors in 8.723s

```

# Install Node plugins
```
sudo npm install mongoose connect-mongo express-session method-override bcrypt-nodejs hat --save
```

# Generate skeleton
    ? express IoT.me
 
# Fetch repo
```
git clone https://github.com/aldem7880/aqua_IoT.git
```

# Install dependencies
```
cd aqua_IoT
sudo npm install
``` 
# Run the app
```
nodemon bin/www
```

______________
# forked from:
## IoT.me
    Make your own data platform for the Internet of Things using Node.js and Express.js

- http://digitaljunky.io/wp-content/uploads/2015/09/IoT.me_landing_login.png

    The tutorial for which the code of this repository was written is available 
    [here](http://digitaljunky.io/make-your-own-data-platform-for-the-internet-of-things-using-node-js-and-express-js).
