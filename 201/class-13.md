# logal 
ersistent local storage is one of the areas where native client applications have held an advantage over web applications. For native applications, the operating system typically provides an abstraction layer for storing and retrieving application-specific data like preferences or runtime state. These values may be stored in the registry, INI files, XML files, or some other place according to platform convention. If your native client application needs local storage beyond key/value pairs, you can embed your own database, invent your own file format, or any number of other solutions.

## What we really want is

1-a lot of storage space<br>
on the client<br>
that persists beyond a page refresh<br>
and isn’t transmitted to the server<br>

## So what is HTML5 Storage? 
Simply put, it’s a way for web pages to store named key/value pairs locally, within the client web browser. Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you. Unlike cookies, this data is never transmitted to the remote web server (unless you go out of your way to send it manually). Unlike all previous attempts at providing persistent local storage, it is implemented natively in web browsers, so it is available even when third-party browser plugins are not.

## check for HTML5 Storage

function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
}

## STORAGE EVENT OBJECT
 |PROPERTY   |	TYPE   |                                  	DESCRIPTION                                                   |
 |-----------|---------|--------------------------------------------------------------------------------------------------|
 |key	     |string   |	the named key that was added, removed, or modified |
 |oldValue	 | any     |	the previous value (now overwritten), or null if a new item was added |
 |newValue   | 	any	   |     the new value, or null if an item was removed |
 |  url*	 |string   |	the page which called a method that triggered this change|

* Note: the url property was originally called uri. Some browsers shipped with that property before the specification changed. For maximum compatibility, you should check whether the url property exists, and if not, check for the uri property instead.


##