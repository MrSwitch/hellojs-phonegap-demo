# Hello.js and Cordova (Phonegap) Demo

This is a demo implementation of [HelloJS](https://github.com/MrSwitch/hello.js/) within a Cordova app.

[Hello.js](https://github.com/MrSwitch/hello.js) is a clientside javascript library to interface with thirdparty API's.


## Demo App

[Android demo release .apk file](dist/android-release-signed.apk)

 
## Setup Demo

It is assumed you are familiar with [cordova development](https://cordova.apache.org/).

Here is your instructions:

	git clone git@github.com:MrSwitch/hellojs-phonegap-demo.git
	cd ./hellojs-phonegap-demo
	cordova plugin add cordova-plugin-inappbrowser
	cordova plugin add cordova-plugin-whitelist

	cd www
	bower install


Next, simply add a platform and run e.g.

	cordova platform add ios
	cordova run ios

# FAQ's

* What's the difference with a typical browser?

HelloJS in Cordova works slight differently because apps run off the local filesystem, not a registered web domain. When registering a `redirect_uri` with an OAuth2 provider we can't simply register a anonymous path like ~~`file://local_assets/redirect.html`~~ - pertaining to the origin of a cordova app. However we can register a legitimate domain, like `https://adodson.com/hello.js/redirect.html` and put that in its stead. On a browser this would not work, because the same-origin rule prevents a file:// path and a http:// path from talking to oneanother (amongst other things).
However we're talking about the special world of in-app-browsers - not a typical browser environment. The cordova plugin InAppBrowser provides an interface in which HelloJS can launch the device's browser and provide an API to monitor and augment that web window. So HelloJS running in the Cordova app triggers the user signin flow, and listens for the right URI (aka value of `redirect_uri`) and extracts the query parameters, tokens, state, etc...

* Does the Redirect page need to include HelloJS script

No, unlike the browser environment its not neccesary for the Redirect page to contain an instance of the HelloJS library. In fact it doesn't actually need to return content at all. However there is a delay between loading the page and notifying the inappbrowser of the page load, a desolate white screen will appear to the user if nothing else. So think about pointing to a simple splash screen.

* What to whitelist

Cordova has some other quirks like requiring the HTTP requests to be whitelisted first. I've whitelist'ed the lot in config.xml file.

	<access origin="*" />
	<allow-intent href="http://*/*" />
	<allow-intent href="https://*/*" />

## Bugs

If you encounter any bugs specifically with HelloJS, please create a ticket at the [Hello.js repo](https://github.com/MrSwitch/hello.js/)
