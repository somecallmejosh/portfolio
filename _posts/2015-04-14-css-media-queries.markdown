---
title:  "CSS Media Queries"
date:   2015-04-14 18:05:48
categories: css
main_image: "cat-in-a-box.jpg"
flickr_attribution: Jeff
flickr_link: https://www.flickr.com/photos/peptic_ulcer/8005951331/in/photolist-dcsApD-bVsnSX-dzyAf-75Asik-788qNz-4NM77F-aBiyQE-7Q9fLj-7pwjEo-fdUY1p-7RtNxW-rcGc4U-6v6xPy-e1ZJgV-4g17qF-A6es-m9ctJ2-7Pyt6d-bsbeJ-iG7mo2-qcL1TD-4NaFnY-e3oPHd-NP2pe-oPGWN3-fDNtzY-bB5JDB-8Etg5F-9ahi5b-dJheQu-qBtgR4-4Fw3iw-6z4PwQ-nE9ef1-mGDyx-mpbD8y-9B4BHv-hiPyZD-7uyV1Q-8ZQ4Bz-5Cmghj-8i7wk3-iDc12h-7ueXvW-99rxva-6d476C-75hz35-5UPURD-78hQQ8-8bG4KN
flickr_license: "https://creativecommons.org/licenses/by-sa/2.0/"
---

Responsive is the big buzz word. Here's the basics on how to use media queries.

## Media Types

* all = all devices, also the default
* print
* screen
* speech

## Media features

* width
* height
* max-width
* max-height
* min-width
* min-height

## Min Screen

{% highlight css %}

@media all (max-width: 960px) {
  /* do something when the browser is < 960px */
  p {
    color: red;
  }
}

@media all (max-width: 480px) {
  /* everything less than 480px */
  p {
    color: blue; 
  }
}

@media all (min-width: 481px) and (max-width: 700px) {
  /* everything between 481px and 700px */
  p {
    font-weight: bold;
  }
}

{% endhighlight %}