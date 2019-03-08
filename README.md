# Capacitor-Introduction

Capacitor Core is a JavaScript library that runs on all platforms that Capacitor supports, and web is no different.

## What do i need to use Capacitor?
Capacitor is made from Ionic Team, but it doesnt need to be an Ionic or Angular project.

Capacitor was designed to drop-in to any existing modern JS web app.

To add Capacitor to your web app, run the following commands:
```Shell
cd my-app
npm install --save @capacitor/core @capacitor/cli
```
Then, init Capacitor with your app information. This will also install the default native platforms.
```
npx cap init
```
## What can i do with Capacitor?
Once we are done with the installation we should be able start transforming our web into any platform app.

### WebJS
You can use it for a Build System Project or a non Build System Project.

- With Build System:
Generally, apps will be using a framework with a build system that supports importing JavaScript modules. In that case, simply import Capacitor at the top of your app and you're set
```
import { Capacitor } from '@capacitor/core';
```

- Without Build System:
To use Capacitor core in a web app that is not using a build system or bundler/module loader, you must set bundledWebRuntime to true in your capacitor.config.json, tell capacitor to copy the specified version of Capacitor Core into your project, and then import capacitor.js into your index.html
```
{
  "bundledWebRuntime": true
}
```
```shell
npx cap copy web
```
### Android

### IOS

### Electron
