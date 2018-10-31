## aqua_IoT
this is fork of IoT.me below.
purpose is to make it work under ubuntu 16.4 LTS and latest nodejs + mongodb.

# TODO:
	- setup vagrant
	- autoconfig with ansible
	- fix errors 

--------------
TypeError: req.body.hasOwnProperty is not a function
    at /root/IoT.me/routes/datasets.js:143:22
    at Layer.handle [as handle_request] (/root/IoT.me/node_modules/express/lib/router/layer.js:95:5)
    at next (/root/IoT.me/node_modules/express/lib/router/route.js:137:13)
    at authenticate (/root/IoT.me/utils.js:4:9)
    at Layer.handle [as handle_request] (/root/IoT.me/node_modules/express/lib/router/layer.js:95:5)
    at next (/root/IoT.me/node_modules/express/lib/router/route.js:137:13)
    at Route.dispatch (/root/IoT.me/node_modules/express/lib/router/route.js:112:3)
    at Layer.handle [as handle_request] (/root/IoT.me/node_modules/express/lib/router/layer.js:95:5)
    at /root/IoT.me/node_modules/express/lib/router/index.js:281:22
    at Function.process_params (/root/IoT.me/node_modules/express/lib/router/index.js:335:12)
    at next (/root/IoT.me/node_modules/express/lib/router/index.js:275:10)
    at Function.handle (/root/IoT.me/node_modules/express/lib/router/index.js:174:3)
    at router (/root/IoT.me/node_modules/express/lib/router/index.js:47:12)
    at Layer.handle [as handle_request] (/root/IoT.me/node_modules/express/lib/router/layer.js:95:5)
    at trim_prefix (/root/IoT.me/node_modules/express/lib/router/index.js:317:13)
    at /root/IoT.me/node_modules/express/lib/router/index.js:284:7
---------------

How to install:

# Install node.js
curl --silent --location https://deb.nodesource.com/setup_0.12 | sudo bash -
^^^^ change to latest nodejs repo

sudo apt-get install --yes nodejs
 
# Install latest stable MongoDB
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10
echo "deb http://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.0.list
sudo apt-get update
sudo apt-get install -y mongodb-org
 
# Install Express-generator
# the -g option is used so that the package is installed globally, 
# meaning that we can now use it from the command line
# Try express -h to see the options now available
sudo npm install express-generator -g
 
# Install Nodemon
sudo npm install nodemon -g

# Install Node plugins
sudo npm install mongoose connect-mongo express-session method-override bcrypt-nodejs hat --save


# Generate skeleton
# express IoT.me
 
# fetch repo
git clone git@github.com:aldem7880/aqua_IoT.git

# Install dependencies
cd aqua_IoT
sudo npm install
 
# Run the app
nodemon bin/www




--------------- forked from:
## IoT.me
Make your own data platform for the Internet of Things using Node.js and Express.js

![alt tag](http://digitaljunky.io/wp-content/uploads/2015/09/IoT.me_landing_login.png)

The tutorial for which the code of this repository was written is available [here](http://digitaljunky.io/make-your-own-data-platform-for-the-internet-of-things-using-node-js-and-express-js).
