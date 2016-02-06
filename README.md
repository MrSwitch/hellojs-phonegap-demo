# Hello.js and Cordova (Phonegap) Demo

This is a demo implementation of [HelloJS](https://github.com/MrSwitch/hello.js/) within a Cordova app.

[Hello.js](https://github.com/MrSwitch/hello.js) is a clientside javascript library to interface with thirdparty API's.


## Demo App

[Android demo release .apk file](dist/android-release-signed.apk)

 
## Setup Demo

It is assumed you are familiar with [cordova development](https://cordova.apache.org/).

Here is the complete list to setup this demo.

	git clone git@github.com:MrSwitch/hellojs-phonegap-demo.git
	cd ./hellojs-phonegap-demo
	cordova platform add ios
	cordova platform add android
	cordova plugin add cordova-plugin-inappbrowser
	cordova plugin add cordova-plugin-whitelist

	cd www
	bower install

Now initiate with `cordova run ios`, or whatever platform you like.

## Bugs

If you encounter any bugs specifically with HelloJS, please create a ticket at the [Hello.js repo](https://github.com/MrSwitch/hello.js/)
