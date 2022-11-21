# Node.js

## What is Node?

-   A way to run JavaScript outsie of the browser. But how JavaScript run in a browser?
-   Browsers have a built-in JavaScript interpreter/engine.
-   Node.js was originally created by Google; they ripped the JS interpreter out of Chrome to fashion Node.

## FS Module

-   It's a built-in library/package that you can import if you want to interact with the device's file system.

## Packages & NPM

-   A package is a library/re-useable module of code/it's code you can share with other people.
-   NPM stands for "Node Package Manager".
-   We can initialize a package (giving the metadata) with the "npm init" command.
-   We can install external packages as dependencies using the command "npm install $PACKAGE1 $PACKAGE2 etc..."
-   By default, the install command installs packages locally. Installed packages are automatically added to the "package.json" file. If you don't already have a 'package.json' file, a new one will be created for you when you try to install something.
-   If we want to mark a package as a devDependency (doesn't need to be included in the built/distribution version of your code), we can add the flag ' -D ' / ' --save-dev '
-   If we want to install a package globally, we can add the ' -g '
-   Packages installed locally are downloaded to a folder called "node_modules". We don't want to share this folder, we only want to share the 'package.json' file that described our dependencies.
-   If you clone a new repo and want to install all the dependencies, type "npm install".
