---
title:  "Simple AJAX Connection"
date:   2015-05-13 19:05:48
categories: javascript
main_image: "ajax.jpg"
flickr_attribution: daveynin.
flickr_link: https://www.flickr.com/photos/daveynin/1672745911/in/photolist-3xPg5K-ydRLp-YWwS-YWwQ-wtX3T-hWctXd-eQ3cY-9YqyAw-eTP8J3-KiV7h-iheTxB-7y3t65-bmdDX-wtVph-wtWiJ-5G3bSU-4V2UHu-7iqcGx-4UXNJP-8vxV6A-vccGq-fs1G4-9w54Z-67CWjZ-7VtQV7-eFyuR-3dk97n-aLjij-oUrTf-q19j8-qBS7T-ZJWQX-6vHHN-rLrUdn-6h882-3htSV7-niHgi-4nG5q6-9w5sx-9w5ob-3g8Myt-5VotyB-3cmXh-376xV-hS6FG1-7ZnCh-5AgsEV-6X6gk-2tdwxR-25PEuq
flickr_license: "https://creativecommons.org/licenses/by/2.0/"
---

Here's my little simplified AJAX connection. Here are the basic steps:

1. Create an XHR Object
1. Create a callback function
  - Use 'Get' when getting or receiving information from a server. 
  - Use 'Post' when sending information to a server that needs to be saved.
1. Open the request
1. Send the request

{% highlight javascript %}
// Create XHR Object
// create a new variable for each request
var xhr = new XMLHttpRequest();

// Create Callback function
// This is what runs when the server sends back its response
// Response to some event
xhr.onreadystatechange = function() {
  if (xhr.readyState === 4) {
    document.getElementById('ajax').innerHTML = xhr.responseText;
  }
}

// Open Request
xhr.open('GET', 'filename.html');

// Send Request
function loadContent(){
  xhr.send();
  document.getElementById('load').style.display = 'none';
} 
    
{% endhighlight %}