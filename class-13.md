# "The Past, Present, and Future of Local Storage for Web Applications"

# Diving In  
*Cookies were invented early in the web’s history, and indeed they can be used for persistent  
local storage of small amounts of data. But they have three potentially dealbreaking downsides:

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
