Building Progressive Web Apps for Android and iOS
-----------------------------------------
*with [Simon MacDonald](https://twitter.com/macdonst)*

Note: speakers are paraphrased

#Core Tenents of a PWA

Response designed - really should be doing this whether you are making a PWA or not  
Connectivity independent - mobile devices have unreliable connections and the app should be built as such  
App Like - app shell model  
Safe - served over https to prevent snooping and ensure content hasn't been tampered with  
Re-engageable - make re-engagement through features like push notifications  
Installable - allow users to add apps to their home screen without the hassle of an app store  
Linkable - easily share the app via url  
Discoverable - manifest.json and service worker registration allow search engines to find and understand your app

#manifest.json
- describes the core elements of the app
- short_name sets the name the OS displays
- start_url sets the starting file for the app, you can set a url param on this so you have a way to track in analytics 
how many people are starting the app from the home screen of their desktop/phone vs users coming via browser
- display sets how the app is shown, ie. standalone removes the browser bar, fullscreen is good for games, etc
- set visual things like background and theme colours, used in various ways by the OS and depending on the display mode
- icons for home, splash, etc screens

#Components of your PWA
- application shells, the framework for your UI/views, these get cached
- content, content is loaded dynamically into the shell
- consider looking at Preact for your PWA framework due to it being incredibly lightweight

#Caching the Application Shell
- this is achieved using [Service Workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API/Using_Service_Workers)
- service worker is a script that your browser runs in the background - only one service worker for domain
- browser installs/registers the service worker
- service worker setups up lists of files to cache and makes that happen
- service worker has several phases: activation (startup), fetch(when the browser requests the app, it checks for cache), 

#workbox
- generates all your service worker boilerplate code
- it can integrate into your IDE or build pipeline
- [Workbox JS](https://workboxjs.org/)

#Lighthouse
- Google product that provides reports on your PWA setup, configuration, etc
- will eventually be integrated into Chrome
- Pro Tip: run Lighthouse using Incognito Mode with all your plugins turned off

#Apple
- support for PWA's in Safari is not really existent
- it ignores your manifest.json
- Safari does however have the ability to add to home screen
- short_name can be set using meta tag in html <meta name="apple-mobile-web-app-capable" content="true">
- your app will need to include UI for a back button as web capable removes all the browser chrome and Apple devices don't have back buttons
- recommend making background color black
- use apple-touch-icon and apple-touch-startup-image for your icons and start screen
- check Jake Archibald's site, [Is Service Worker Ready](https://jakearchibald.github.io/isserviceworkerready/)?

In the meantime, you can use Cordova to and the [phonegap-plugin-pwa](https://github.com/phonegap/phonegap-plugin-pwa) to build your PWA's as iOS apps.
If you need to add Service Worker support you can use this [phonegap-plugin-serviceworker](https://github.com/phonegap/phonegap-plugin-service-worker)

See [Service Worker Cookbook](https://serviceworke.rs/) for examples of other PWA's
