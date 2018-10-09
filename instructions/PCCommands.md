## Configure git

Enter these commands in your terminal in VSCode

`git config --global user.name "YourName`
`git config --global user.email "YourEmail"`

## MongoDB Installation

### Get The Install Package

1. Visit https://www.mongodb.com/dr/fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.2-signed.msi/download
3. Navigate to your downloads folder; double click mongodb-win32-x86_64-2000plus-ssl-4.0.2-signed
4. Follow all the instructions to install MongoDB. Choose all defaults.

### Open a command prompt as an administrator:

1. Search for cmd.exe in the search bar
2. Type [Ctrl] [Shift] [Enter] to open the command prompt in admin mode
3. Say YES to allow your computer to make changes

#### Once you have totally finished installing MongoDB, make the database by entering this in the command prompt (you will only do this step ONCE):

```shell
md "\data\db" "\data\log"
```

### Start mongoDB by entering this (every time you need to start MongoDB):

```shell
"C:\Program Files\MongoDB\Server\4.0\bin\mongod.exe" --dbpath="c:\data\db"
```

// Expected Output:

```shell
2018-10-08T14:21:00.694-0400 I CONTROL  [initandlisten] db version v4.0.2
2018-10-08T14:21:00.694-0400 I CONTROL  [initandlisten] git version: fc1573ba18aee42f97a3bb13b67af7d837826b47
2018-10-08T14:21:00.694-0400 I CONTROL  [initandlisten] allocator: system
2018-10-08T14:21:00.694-0400 I CONTROL  [initandlisten] modules: none
2018-10-08T14:21:00.694-0400 I CONTROL  [initandlisten] build environment:
2018-10-08T14:21:00.694-0400 I CONTROL  [initandlisten]     distarch: x86_64
2018-10-08T14:21:00.694-0400 I CONTROL  [initandlisten]     target_arch: x86_64
2018-10-08T14:21:00.694-0400 I CONTROL  [initandlisten] options: {}
(lots more)
```

#### Open another admin command prompt by following the steps above

#### Enter this command in the new command prompt:

```shell
"C:\Program Files\MongoDB\Server\4.0\bin\mongo.exe"
```

// Expected Output:
```shell
MongoDB shell version v4.0.2
connecting to: mongodb://127.0.0.1:27017/mongo
MongoDB server version: 4.0.2

(there may be some warnings here; you can ignore these)

_ _ _
>
```

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

4. Copy and paste that command into the terminal in Visual Studio Code
