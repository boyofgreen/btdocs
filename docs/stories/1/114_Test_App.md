# Task 1.1.4 - Install App Locally for Testing

## Prerequisites 

This task has a dependency on [Task 1.1.3](113_ConfigureSW.md) and all of it's prerequisites

## Task 

### Test the App in Browsers

The first thing you want to do is make sure your PWA works well in the browser.  One of the main principles of PWAs is that the app must be "Progressive".  This means the app should work in any environment, then start taking advantage of advanced features (such as service workers and app manifest) when they are available.  In normal circumstances, you would want to test your app in the array of browsers used by your user.   To get you started, we have the newest version of Edge (with service worker support) available to you for free on browser stack  

**NOTE** for Dry Run Users, Edge 16 may not yet be available in browser stack.  You can test the service worker code in chrome **END NOTE**

1.  In your browser, visit https://www.browserstack.com/test-on-microsoft-edge-browser

2. Create an account if you don't already have one.

3. Choose Windows > 10 > Edge 16 > new session to get started testing in Edge
!(image of browser stack select)

4. You can also use browser stack to test in other browsers you don't have installed on your device (trial limitations apply)

5. to test the service worker, simply visit a number of pages with the service worker attached to your app, and each page will be added to the cache (don't worry the service worker will always keep itself up to date).  You can then go offline and see each of those pages still work fine without a connection.  If you are using BrowserStack and can't go offline, simply open up the f12 tooling in the browser, and you can validate that the service worker is caching it's content by the logs in the console.

### Install Windows Store PWA locally
The next environment you'll want to test in, is the local PWA.  To do this we'll use more tools from PWABuilder.com

1. In the browser, open www.pwabuilder.com/generator.

2. Enter your site URL and press "get started".  If you have your manifest properly linked to your page, you should see the data from your manifest (including images) show up in the builder.

3. Click on the 3rd tab called "Publish PWA".  This time you'll click on the "Download" button under "Windows" to get the source code

4. Inside the zip, decompress it and navigate to \PWA\Store packages\windows10 and right click on the "test_install" script and choose "run powershell script"

5. Follow the prompts to "side load the application".

6. open the app from your start screen / start menu.  Your now experiencing your PWA on Windows 10!

### F12 with Windows Store PWA

Your app is sideloaded on your machine, which means it's in debug mode.  While PWAs are in debug mode on Windows 10, you have access to the same f12 tools you do while in the Edge browser.  While the app in forefront on your screen, hit the "f12" button on your keyboard and the tools should open.

## References
https://www.pwabuilder.com/generator

https://www.browserstack.com/test-on-microsoft-edge-browser


## continue to [next task >> ](121_Add_WIndows_Feature.md)





