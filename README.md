# vagrant_where_you_at_server

Vagrant project files to set up the NodeJS/MongoDB box for development of the WhereYouAt server.

## Pre-requisites
To use this project, you must first have Vagrant installed and working. Please visit [vagrantup.com](https://vagrantup.com) for more information. Especially ensure that the command `vagrant ssh` works for Vagrant boxes.

## Preparation
Before running, this Vagrant project and the [where_you_at_server](https://github.com/TVSD/where_you_at_server) must be cloned into the correct locations.

1. Create a `server` folder which will contain this project & the where_you_at_server project.
2. In the `server` folder, clone the `where_you_at_server` project. You should now have a `server\where_you_at_server` folder.
3. In the `server` folder, clone this project. You should now have a `server\vagrant_where_you_at_server` folder.
4. You should now have the following directory structure:

   ```
   server\
     where_you_at_server\
     vagrant_where_you_at_server\
   ```
5. Be sure to copy `where_you_at_server\config.js.example` to `where_you_at_server\config.js` and edit the `where_you_at_server\config.js` file with the appropriate settings for you installation.

## Running the Node project (quick)
1. `vagrant up` in the `server\vagrant_where_you_at_server` folder.
2. `vagrant ssh`
3. `cd /server && npm install --no-bin-links && npm start`

## Running the Node project (detailed)
1. Open the `server` folder in your command prompt.

   On Windows, you can double-click the `server` folder in Explorer, shift+right-click in an empty area of the folder and select "Open command window here".
2. Change directories to the `vagrant_where_you_at_server` folder:

   ```
   cd vagrant_where_you_at_server
   ```

3. Start the Vagrant box using the command `vagrant up`
4. Once the box has loaded, SSH into the Vagrant box using the command `vagrant ssh`
5. You should now be at a command prompt within the Vagrant VM:

   ```
   Welcome to Ubuntu 14.04.1 LTS (GNU/Linux 3.13.0-35-generic x86_64)

   vagrant@vagrant-ubuntu-trusty-64:~$
   ```

6. At the Vagrant box's Linux command prompt, change directories to the NodeJS project directory:

   ```
   vagrant@vagrant-ubuntu-trusty-64:~$ cd /server
   ```

7. Run the project:

   ```
   vagrant@vagrant-ubuntu-trusty-64:/server$ npm install --no-bin-links
   vagrant@vagrant-ubuntu-trusty-64:/server$ npm start
   ```
