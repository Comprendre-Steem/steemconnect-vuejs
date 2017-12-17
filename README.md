# SteemConnect v2 demo app

This simple project has been created to learn and demonstrate the usage of SteemConnect v2.

## Dependencies

This project uses multiple dependencies:
- jQuery (+ cookies plugin)
- SteemJS
- SteemConnect v2
- VueJS

## Usage

First, clone the repository: 

> git clone https://github.com/Comprendre-Steem/steemconnect-vuejs.git

Go to that new directory:

> cd steemconnect-vuejs

Then start and http server to access the project.
Use your favority server (therefor you could use WAMP/LAMP/httpd/...)

This a very simple example with docker httpd image:

> docker run -d --name httpd -p 80:80 -v "$PWD":/usr/local/apache2/htdocs/ httpd

You can now access the demo on http://localhost/

Clicking on the *Login* link will redirect to the SteemConnect Autorisation page.
After entering your credentials, you should be redirected to http://localhost/steemconnect/ which will keep the access_token as a cookie and redirect you to the main application (http://localhost/).

The application will detect the cookie and attemp to log you in.
On success you should see three fields (username, reputation and creation date) and two buttons (un/follow @comprendre-steem).

## SC2Utils.js

The main interaction that can be performed on the blockchain are made available using the SC2Utils.js file.
You can see example of use in the main application (js/App.js).

## Screenshot 

![](https://steemitimages.com/DQmaYdq4VW7sLBng1821qXDnVannGUmaRv6fgACjqXEUN5q/image.png)

## Demo

A live demo is available on : http://steemconnect.surge.sh/