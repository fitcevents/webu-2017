From AMP to PWA: A Modern Web User Journey
--------------------------------------
*with Alberto Medina*

The typical user acquisition cost for a native app is expensive. From getting the app built and tested, to the delivery, to 
getting users to install and use the app, everything is costly. A PWA is a fraction of the cost.

Native apps, once installed, are always there, always start, in the same amount of time. Mobile web apps only work well if you 
have fast reliable wifi. Yet, in mobile web intermitent and flaky wifi is the norm.

This is where PWA's fit in. The introduction of the Service Worker is the solution, the core of the PWA. It's javascript that 
can intercept all requests and determine what to do with them: go to the server, hit a local cache or something else. 

Even with a PWA you can only use a service worker after the first visit to a website. We have to still be careful then to not 
make the initial page load too heavy. 

The solution (from Google) is AMP (Accelerated Mobile Pages). AMP is an opne source initiative, made of of AMP-HTML, AMP JS and AMP Cache. AMP-HTML is both a 
sub and super set of HTML. Some html tags (iframe) and not available in AMP while at the same time it adds a series of features
for the highspeed delivery of pages.

##AMP Features
- everything is loaded aysnc
- no custom js allowed
- uses a static layout system (every detail about a page layout is detailed 
beforehand so the browser has nothing to figure out)
- prioritized content loading
- inline, size-bound CSS
- Web Font optimizations
- Min style/reclacs
- GPU based animations

##AMP Cache
- this is a CDN for AMP pages
- primarily Google CDN right now, doesn't have to be
- cache is optional
- cache provides validation
- uses http/2.0
- does pre-rendering giving an instant load feeling

##AMP or PWA
PWA requires a service worker, but AMP doesn't allow custom js, so how do we do this?

There are three integration points to do this:
- AMP to Progressive Web App
- AMP as Progressive Web App
- AMP in Progressive Web App

###AMP to PWA
<amp-install-serviceworker> this allows a user to discover content from search or social, display an AMP page and then moves
to installing the Service Worker and loading a PWA. ie. Rakuten is doing this with recipe ddiscovery on AMP to recipe app in PWA.

###AMP as PWA
[ampbyexample.com](http://ampbyexample.com)

###AMP in PWA
AMP pages aaren't just web pages, they're ultra-portable, embeddable, content units. Facebook, Twitter, etc, make use of this 
for displaying AMP pages.

Similary we can load AMP pages into a PWA ourselves. PWA has an application shell that is cached. Then the content is loaded as 
AMP pages into the shell. Allows you to create a separation between app architecture and the content delivery. In this way 
AMP pages can exist on their own or as content in a PWA.

You could load AMP into an iframe, but it's slow. The Shadow DOM is the solution. 

Example: [http://goo.gl/zs42rs](http://goo.gl/zs42rs)

Or check the Shadow Reader App. It's a serverless SPA.
- uses two app shell architectures
- loads Guardian AMP pages
- provides full URL-based nav using History API
- 60fps page transitions
- cross browser
- app is under 10kb

The PWA portion of this uses [workboxjs.org](workboxjs.org) to make the Service Worker implementation easier. Workbox provides 
both code libraries to build your application and build tools as well.

App determines the skeleton UI shell to use based on the url requested. Keeping them separate keeps the app small and fast.

Ultimately you can use AMP beyond PWA's - it can also be used to deliver content to native Android or iOS.




