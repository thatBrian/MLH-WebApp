## Commands to Install MongoDB

// install homebrew

/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

// install mongoDB

brew install mongodb

// create database files

sudo mkdir -p /data/db

## Commands to Start MongoDB

// run mongodb

sudo mongod

// Expected Output:

// in another terminal:

mongo --host 127.0.0.1:27017

// Notes

## Deploy Your App

### Keys

1. Go to
2. Copy and Paste Keys Here So You Don't Lose them:

* username:
* primary password:
* host:
* port:

3. Also, retrieve what you named your database. You can find this by going to Resource Groups -> (The resource group you created today) -> Then noting the name of the Azure CosmosDB Account below:

* database:

It will be much easier to use the command below if you replace all the values in here and THEN copy and paste it into your Azure portal.

`mongodb://<username>:<primary password>@<host>:<port>/<database>?ssl=true&replicaSet=globaldb`


### Git URL
1. Go to portal.azure.com -> Resource Groups -> (The resource group you created today) -> (the APP SERVICE resource).
2. On the right side of the window, there will be "URL," "App Service plan/pricing tier, Git/Deployment username, Git clone url, and FTP hostname.
3. Copy the Git clone URL and replace YOUR URL HERE with it (below).

`git remote add origin YOUR URL HERE`


## TroubleShooting

### Error 1:

### Error 2:
