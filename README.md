# Professional iOS Network Programming
## Chapter 2: Service Architecture

The example code from Chapter 2 of my book, [Professional iOS Network Programming](http://www.wiley.com/WileyCDA/WileyTitle/productCd-1118362403,descCd-description.html "Professional iOS Network Programming: Connecting the Enterprise to the iPhone and iPad").  Further discussion is also available on the [Wiley P2P forum](http://p2p.wrox.com/book-professional-ios-network-programming-connecting-enterprise-iphone-ipad-708/).

* Facade PHP is a web service that serves stock ticker and weather data to clients.  Each endpoint is built with two completely independent data sources that are converted to a common output format.  Thus, the backend system can be completely replaced and the service output will remain unchanged.  Each endpoint also has a second version that adds and changes the type of some fields, demonstrating how multiple app versions can be deployed after service enhancements are made.

* Facade Tester is a corresponding iOS app that consumes a service locator to discover the proper Facade PHP endpoints to use and then displays API results in a table view.  A segmented control allows the app to change which service version it consumes.

Once the PHP services are running, be sure to update the service locator URL in `FTAppDelegate loadServiceLocator`.