# Hello.js and PhoneGap Demo

This is a demo implementation of [HelloJS](https://github.com/MrSwitch/hello.js/) within a PhoneGap app.

[Hello.js](https://github.com/MrSwitch/hello.js) is a library which lets clients connect with thirdparty API's within your app. Phonegap is Phonegap.

## Setup this demo app

* See the guide for [setting up a new phonegap application](http://docs.phonegap.com/en/edge/guide_cli_index.md.html) 
* Clone this demo into the `www/` directory - replacing its content.
* Download [HelloJS](https://github.com/MrSwitch/hello.js/) into `www/components/hello/` folder. If you use bower then run `cd www/` and `bower install hello --save` for the same effect.
* Install [InAppBrowser](http://cordova.apache.org/docs/en/3.1.0/cordova_inappbrowser_inappbrowser.md.html) plugin - I installed it using `phonegap plugin add https://git-wip-us.apache.org/repos/asf/cordova-plugin-inappbrowser.git`.

## Update an existing phonegap app
HelloJS requires a phonegap app to meet the following conditions...

* Include HelloJS into project, You can either use bower e.g. `bower install hello --save` or manually download [HelloJS](https://github.com/MrSwitch/hello.js) and include where you like e.g.  `path/to/myPhonegapApp/www/bower_components/hello.js/` folder.
* Embed `<script src="./bower_components/hello.js/dist/hello.all.js">` tag in your HTML page
* Provision `<access origin="*" />` in the phonegaps [config.xml](config.xml) file
* Insure [InAppBrowser](http://cordova.apache.org/docs/en/3.1.0/cordova_inappbrowser_inappbrowser.md.html) plugin is available - I installed it using `phonegap plugin add https://git-wip-us.apache.org/repos/asf/cordova-plugin-inappbrowser.git` - and include `<gap:plugin name="org.apache.cordova.inappbrowser" />` in  phonegap's [config.xml](config.xml) file if you haven't already.

## Bugs

If you encounter any bugs please create a ticket at the [Hello.js repo](https://github.com/MrSwitch/hello.js/)
