# Hubl.in

[![Join the chat at https://gitter.im/linagora/hublin](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/linagora/hublin?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[![Code Climate](https://codeclimate.com/github/linagora/hublin/badges/gpa.svg)](https://codeclimate.com/github/linagora/hublin)
[![Build Status](https://travis-ci.org/linagora/hublin.svg?branch=master)](https://travis-ci.org/linagora/hublin)

[Hubl.in](https://hubl.in) is a free and open source video conference solution built with love and designed with ethics in mind.
It's the best way to initiate a communication anywhere with anybody and brings real time conversation to the next level.
Hubl.in allows free communication without additional plugins.

## Installation

1. clone the repository

        git clone --recursive https://ci.open-paas.org/stash/scm/meet/meetings.git

2. Install and configure MongoDB

  You must install mongoDB. We suggest you to use mongoDB version 2.6.5.

        echo 'deb http://downloads-distro.mongodb.org/repo/debian-sysvinit dist 10gen' | tee /etc/apt/sources.list.d/mongodb.list
        apt-get install -y mongodb-org=2.6.5 mongodb-org-server=2.6.5 mongodb-org-shell=2.6.5 mongodb-org-mongos=2.6.5 mongodb-org-tools=2.6.5
        service mongod start

3. install node.js

  We are currently using Node 6. It is highly recommended that you use [nvm](https://github.com/creationix/nvm) to install a specific version of node.

4. Install Redis

        apt-get install redis-server

5. Copy the sample db.json configuration file and adapt it to your need (especially the mongodb URL if you do not use default parameters from step 2)

        cp config/db.json.sample config/db.json

6. Install the npm dependencies (as an administrator)

        npm install -g mocha grunt-cli bower karma-cli

7. Go into the modules directory and install easyrtc  and Janus connector module dependecies

        cd modules/hublin-easyrtc-connector
        npm install
				cd modules/hublin-janus-connector
        npm install

8. Go into the project directory and install project dependencies

        cd meetings
        npm install

9. Install and run Janus Gateway 
				
				check this Link : https://github.com/meetecho/janus-gateway


## Starting the server

Use npm start to start the server !

    npm start

the server will Start on : localhost:8080

## License

[Affero GPL v3](http://www.gnu.org/licenses/agpl-3.0.html)
