# Hello.js and PhoneGap Demo

[Hello.js](https://github.com/MrSwitch/hello.js) is a library which lets clients connect with thirdparty API's within your app. Phonegap is Phonegap.

This is a demo site mashing hello.js into a phonegap app.

# Prerequistes

* Install the feature-phonegap branch from hello.js, try `bower install`
* Provision `<access origin="*" />` in your phonegaps config.xml file (if you haven't already)
* Insure InAppBrowser plugin is available, try `phonegap plugin add https://git-wip-us.apache.org/repos/asf/cordova-plugin-inappbrowser.git` and include `<gap:plugin name="org.apache.cordova.inappbrowser" />` in  phonegap's [config.xml](config.xml) file (if you haven't already)

# Setup
Follow the example in [index.html](index.html). Embedding script tags linking hello.js file and any service from the modules/ dir - e.g. google.js, windows.js.
