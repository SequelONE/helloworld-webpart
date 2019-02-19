# helloworld-webpart

Download and install [Node.js](https://nodejs.org/).

## Fix for Node.js

### Fix for yo

1. Install the latest version of node
2. Install the latest version of npm: **npm i -g npm@next**
3. Run the following in your cmd window or commander window:
```
call npm uninstall -g chalk
call npm uninstall -g loadash
call npm uninstall -g tar-fs
call npm uninstall -g update-notifier
call npm uninstall -g yeoman-generator
call npm uninstall -g yosay
call npm uninstall -g yo
call npm uninstall -g gulp
call npm uninstall -g @microsoft/generator-sharepoint

call npm install -g chalk
call npm install -g loadash
call npm install -g tar-fs
call npm install -g update-notifier
call npm install -g yeoman-generator
call npm install -g yosay

call npm install -g yo
call npm install -g gulp

call npm install -g @microsoft/generator-sharepoint
```

### Downgrade NPM version for SPFx 1.7.0

1. Luckily we have the [Node Version Manager for Windows](https://github.com/coreybutler/nvm-windows/releases) (Use the nvm-setup.zip). 
Install the latest version from this site. The installation is very easy. Just follow the the Setup Wizard.

2. Open your favourite CMDer.
Type in the following for a 64 bits Windows:
```
nvm install 8.9.4 64
```
Now the NVM is downloading the NPM version v5.6.0. Please wait until Installation complete.

3. After the installation is complete type the following in order for using the older version:
```
nvm use 8.9.4
```

### Node Sass could not find a binding for your current environment: Linux 64-bit with Node.js 8.x

This error comes when you have an updated node version but the project which you are running still has the old version. So, probably can use the command
```
npm rebuild node-sass --force
```

### Error when running gulp serve in SPFX

If the local version of gulp is 4.0.0 then change into the package.json and make the configuration to 3.9.1 and try **npm install --save** and then try **gulp serve**