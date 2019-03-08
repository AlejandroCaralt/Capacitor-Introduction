# Capacitor-Introduction

Capacitor Core is a JavaScript library that runs on all platforms that Capacitor supports, and web is no different.

## What do i need to use Capacitor?
Capacitor is made from Ionic Team, but it doesnt need to be an Ionic or Angular project.You can use it for a Build System Project or a non Build System Project.

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
```
npx cap copy web
```
