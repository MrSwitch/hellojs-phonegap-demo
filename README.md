# Hello.js and Cordova/PhoneGap Demo

This is a demo implementation of [HelloJS](https://github.com/MrSwitch/hello.js/) within a PhoneGap app.

[Hello.js](https://github.com/MrSwitch/hello.js) is a library which lets clients connect with thirdparty API's within your app. Phonegap is synonymous with Cordova for the purpose of this demo.


## Demo App

[Android demo release .apk file](dist/android-release-signed.apk)

 
## Setup Demo

See the guide for [setting up a new phonegap application](http://docs.phonegap.com/en/edge/guide_cli_index.md.html) 

	cordova create hello-cordova
	cd hello-cordova
	cordova platform android ios
	cordova plugin add cordova-plugin-inappbrowser
	cordova plugin add cordova-plugin-whitelist

	rm -rf ./config.xml www
	git clone git@github.com:MrSwitch/hellojs-phonegap-demo.git www


## Cordova Dependencies

### Whitelist:

Install

	cordova plugin add cordova-plugin-whitelist`

Insert into [config.xml](config.xml)

	<access origin="*" />


### InAppBrowser: 

Install

	cordova plugin add cordova-plugin-inappbrowser

Insert into [config.xml](config.xml)

	<gap:plugin name="org.apache.cordova.inappbrowser" />


## Install HelloJS

	cd www/
	bower install hello --save

See [index.html](index.html) as an example implmentation of HelloJS


## Bugs

If you encounter any bugs specifically with HelloJS, please create a ticket at the [Hello.js repo](https://github.com/MrSwitch/hello.js/)
