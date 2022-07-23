# BotMan Web Widget

# Custom modifications

You can find a fullscreen version of this, it makes the API accessible via window objects (window.chatInstance for the chat uu where you can execute instrucions to send messages to the bot, sat as bot, etc..)

``` js
window.chatInstance.sayAsBot('Hey dude!, helcome to Cut developments, how may i assist you?')
 ```

You have access to the botman instance where you can setup the hostname of the chatbot instance, here is an example used on the chatbot studio project used in rurusi.

``` js 
window.BotmanInstance.chatServer = "http://127.0.0.1:8000/api/botman" 
```

NOTE: you should always setup your chat server before using it, point it to the exposed route to your web driver, it is "/api/botman" on the updated botman studio.

## Install requirements

### Install nodejs
```
apt-get install build-essential libssl-dev
apt-get install nodejs
nodejs -v
apt-get install npm
npm -v
```

### Install nvm

To download the nvm installation script from the project's GitHub page, you can use curl. Note that the version number may differ from what is highlighted here:

```
curl -sL https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh -o install_nvm.sh
```

Inspect the installation script with nano:

```
nano install_nvm.sh
```

Run the script with bash:

```
bash install_nvm.sh
```

It will install the software into a subdirectory of your home directory at ~/.nvm. It will also add the necessary lines to your ~/.profile file to use the file.

To gain access to the nvm functionality, you'll need to either log out and log back in again or source the ~/.profile file so that your current session knows about the changes:

```
source ~/.profile
```

With nvm installed, you can install isolated Node.js versions. For information about the versions of Node.js that are available, type:

```
nvm ls-remote
```

Then you can use nvm to install the node version you need

```
nvm use <version>
```


### On Mac via homebrew:

```
brew install npm
brew install nvm
```

## Build the widget

```
cd <path_to_widget>
npm install -g grunt-cli
npm install -g webpack
npm install -g bower
npm install -g gulp
npm install preact
npm install
npm run-script build
```
