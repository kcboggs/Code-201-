# "The Past, Present, and Future of Local Storage for Web Applications"

# Diving In  
*Cookies were invented early in the web’s history, and indeed they can be used for persistent  
local storage of small amounts of data. But they have three potentially dealbreaking downsides:*

- Cookies are included with every HTTP request, thereby slowing down your web application by  
needlessly transmitting the same data over and over
- Cookies are included with every HTTP request, thereby sending data unencrypted over the internet  
(unless your entire web application is served over SSL)
- Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but  
not enough to be terribly useful  

What we really want is  

- a lot of storage space  
- on the client  
- that persists beyond a page refresh  
- and isn’t transmitted to the server  

*Before HTML5, all attempts to achieve this were ultimately unsatisfactory in different ways.*  

# A BRIEF HISTORY OF LOCAL STORAGE HACKS BEFORE HTML5  
*userData allows web pages to store up to 64 KB of data per domain, in a hierarchical XML-based  
structure. (Trusted domains, such as intranet sites, can store 10 times that amount. And hey,  
640 KB ought to be enough for anybody.) IE does not present any form of permissions dialog, and  
there is no allowance for increasing the amount of storage available.*  

# INTRODUCING HTML5 STORAGE  
*So what is HTML5 Storage? Simply put, it’s a way for web pages to store named key/value pairs locally,  
within the client web browser. Like cookies, this data persists even after you navigate away from the web site,  
close your browser tab, exit your browser, or what have you. Unlike cookies, this data is never transmitted to  
the remote web server (unless you go out of your way to send it manually). Unlike all previous attempts at providing  
persistent local storage, it is implemented natively in web browsers, so it is available even when third-party browser  
plugins are not.*  

Which browsers? Well, the latest version of pretty much every browser supports HTML5 Storage… even Internet Explorer!  

HTML5 STORAGE SUPPORT  
IE	  FIREFOX	 SAFARI	CHROME	OPERA	IPHONE	ANDROID  
8.0+	 3.5+	    4.0+	 4.0+	  10.5+	 2.0+	   2.0+  

From your JavaScript code, you’ll access HTML5 Storage through the localStorage object on the global window object.  
Before you can use it, you should detect whether the browser supports it.  

↶ check for HTML5 Storage  

function supports_html5_storage() {  
  try {  
    return 'localStorage' in window && window['localStorage'] !== null;  
  } catch (e) {  
    return false;  
  }  
}  

Instead of writing this function yourself, you can use Modernizr to detect support for HTML5 Storage.  

if (Modernizr.localstorage) {  
  // window.localStorage is available!  
} else {  
  // no native support for HTML5 storage :(  
  // maybe try dojox.storage or a third-party solution  
}  

# USING HTML5 STORAGE  
*HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can  
retrieve that data with the same key. The named key is a string. The data can be any type supported  
by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored  
as a string. If you are storing and retrieving anything other than strings, you will need to use  
functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype.*  

interface Storage {  
  getter any getItem(in DOMString key);  
  setter creator void setItem(in DOMString key, in any data);  
};  

Calling setItem() with a named key that already exists will silently overwrite the previous value.   
Calling getItem() with a non-existent key will return null rather than throw an exception.  

Like other JavaScript objects, you can treat the localStorage object as an associative array.   
Instead of using the getItem() and setItem() methods, you can simply use square brackets.  

For example, this snippet of code:  

var foo = localStorage.getItem("bar");  
// ...  
localStorage.setItem("bar", foo);  

…could be rewritten to use square bracket syntax instead:  

var foo = localStorage["bar"];  
// ...  
localStorage["bar"] = foo;  

*There are also methods for removing the value for a given named key, and clearing the entire  
storage area (that is, deleting all the keys and values at once).*  

interface Storage {  
  deleter void removeItem(in DOMString key);  
  void clear();  
};  

Calling removeItem() with a non-existent key will do nothing.    

*Finally, there is a property to get the total number of values in the storage area, and to iterate  
through all of the keys by index (to get the name of each key).*

interface Storage {  
  readonly attribute unsigned long length;  
  getter DOMString key(in unsigned long index);  
};  

If you call key() with an index that is not between 0–(length-1), the function will return null.  

# TRACKING CHANGES TO THE HTML5 STORAGE AREA  
*If you want to keep track programmatically of when the storage area changes, you can trap the storage  
event. The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is  
called and actually changes something. For example, if you set an item to its existing value or call  
clear() when there are no named keys, the storage event will not fire, because nothing actually changed  
in the storage area.*  

*The storage event is supported everywhere the localStorage object is supported, which includes Internet Explorer 8. IE 8 does not support the W3C standard addEventListener (although that will finally be added in IE 9). Therefore, to hook the storage event, you’ll need to check which event mechanism the browser supports. (If you’ve done this before with other events, you can skip to the end of this section. Trapping the storage event works the same as every other event you’ve ever trapped. If you prefer to use jQuery or some other JavaScript library to register your event handlers, you can do that with the storage event, too.)*  

if (window.addEventListener) {  
  window.addEventListener("storage", handle_storage, false);  
} else {  
  window.attachEvent("onstorage", handle_storage);  
};  

The handle_storage callback function will be called with a StorageEvent object, except in Internet Explorer  
where the event object is stored in window.event.  

function handle_storage(e) {  
  if (!e) { e = window.event; }  
}  

At this point, the variable e will be a StorageEvent object, which has the following useful properties.  

STORAGEEVENT OBJECT
PROPERTY	TYPE	DESCRIPTION
key	string	the named key that was added, removed, or modified
oldValue	any	the previous value (now overwritten), or null if a new item was added
newValue	any	the new value, or null if an item was removed
url*	string	the page which called a method that triggered this change
* Note: the url property was originally called uri. Some browsers shipped with that property before the specification changed. For maximum compatibility, you should check whether the url property exists, and if not, check for the uri property instead.
