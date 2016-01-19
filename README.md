# Hello.js and Cordova/PhoneGap Demo

This is a demo implementation of [HelloJS](https://github.com/MrSwitch/hello.js/) within a PhoneGap app.

[Hello.js](https://github.com/MrSwitch/hello.js) is a library which lets clients connect with thirdparty API's within your app. Phonegap is synonymous with Cordova for the purpose of this demo.


## Demo App

[Android demo release .apk file](dist/android-release-signed.apk)

 
## Setup Cordova

See the guide for [setting up a new phonegap application](http://docs.phonegap.com/en/edge/guide_cli_index.md.html) 

If you want to clone this demo into the `www/` directory, replacing its content. However i recommend just copying over the few files to your sample apps www/ directory.


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

If you encounter any bugs please create a ticket at the [Hello.js repo](https://github.com/MrSwitch/hello.js/)
