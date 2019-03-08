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

### Progressive Web App
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
By default, an Android project is created for every Capacitor project. If you are adding Capacitor to an existing project, you can manually add the Android project using
```
npx cap add android
npx cap sync
```
The sync command updates dependencies, and copies any web assets to your project. You can also run
```
npx cap copy
```
To copy web assets only, which is faster if you know you don't need to update native dependencies.

Opening Android Project
To open the project in Android Studio, run
```
npx cap open android
```

### IOS

By default, an iOS project is created for every Capacitor project. If you are adding Capacitor to an existing project, you can manually add the iOS project using
```
npx cap add ios
npx cap sync
```
The sync command updates dependencies, and copies any web assets to your project. You can also run
```
npx cap copy
```
To copy web assets only, which is faster if you know you don't need to update native dependencies.

Opening iOS Project
To open the project in Xcode, run
```
npx cap open ios
```
### Electron

After creating a new Capacitor app, add the electron platform:
```
npx cap add electron
```
This will generate a new Electron project in the electron/ folder in the root of your app.

Preparing your app
Just like the other Capacitor platforms, the copy command must be run periodically to sync web content with Electron:
```
npx cap copy
```
Run this after making any modifications to your web app.

Running your App
To run your app, cd into it and use the npm script provided by Capacitor:
```
cd electron/
npm run electron:start
```
