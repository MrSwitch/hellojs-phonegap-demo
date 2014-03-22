# Hello.js and PhoneGap Demo

This is a demo implementation of Hello.js within a PhoneGap app.

[Hello.js](https://github.com/MrSwitch/hello.js) is a library which lets clients connect with thirdparty API's within your app. Phonegap is Phonegap.

## Setup this demo

* Install the [feature-phonegap](https://github.com/MrSwitch/hello.js/tree/feature-phonegap) branch from Hello.js into your `www/components/hello/` folder. If you use bower then run `bower install` for the same effect.

## Demo notes
HelloJS requires a phonegap app to meet the following conditions...

* Embed `<script src="path_to/hello.js/dist/hello.all.js">` tag, for a comprehensive implementation, else select from the `path_to/hello.js/src/` directory - example at [index.html](./index.html)
* Provision `<access origin="*" />` in the phonegaps [config.xml](config.xml) file
* Insure [InAppBrowser](http://cordova.apache.org/docs/en/3.1.0/cordova_inappbrowser_inappbrowser.md.html) plugin is available - I installed it using `phonegap plugin add https://git-wip-us.apache.org/repos/asf/cordova-plugin-inappbrowser.git` - and include `<gap:plugin name="org.apache.cordova.inappbrowser" />` in  phonegap's [config.xml](config.xml) file if you haven't already.

## Bugs

If you encounter any bugs please create a ticket at the [Hello.js repo](https://github.com/MrSwitch/hello.js/)
