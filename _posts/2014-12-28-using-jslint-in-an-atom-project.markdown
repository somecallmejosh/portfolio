---
title:  "Using .jslintrc In an Atom Project"
date:   2014-12-28 16:41:48
categories: javascript
main_image: "pointer.jpg"
flickr_attribution: Dave Rutt
flickr_link: https://www.flickr.com/photos/rutty/492385781/in/photolist-KvB92-ebvBCm-ebpZ7V-cVEQgq-7o9Qtk-ebpZ86-ebvBAU-ebvBCq-ebpZ8P-ebvBB3-ebpZ94-ebvBCd-5TWEfA-964xgo-9fNJoC-dj9zWT-5c6cXV-p81wB4-bnbSXw-iceN15-8M8pmQ-5tCY8a-79cuaD-aDgz5q-5oECWY-d14FaJ-jDHz3E-5g27x1-51Npnn-4xZPkC-cqQLp7-daft9m-87NNJY-4StYmp-x1Qbv-h1kMBZ-cqQLCS-4BLF5c-6ueaja-cqQLxW-pnFrHJ-BsZbA-bDNMNU-pheRK3-h6R8go-nc5DQ5-jpXHeV-Ckz6U-dFRxY3-79DZkN
flickr_license: "https://creativecommons.org/licenses/by-nc-nd/2.0/"
---


[Atom.io](https://atom.io/) has recently become my favorite editor. It’s every bit as powerful as [Sublime](http://www.sublimetext.com/), and it’s free. There are a bunch of extensions that can be added to the editor to customize it to your needs. JSLint is one of those extensions. What’s JSLint?

[JSLint](http://www.jslint.com/) is a useful tool for making sure your javascript stays nice and clean. However, there are a couple of little issues that come into play that can appear as errors in your project. For instance, if you use the Jquery “$” in a file other than jquery.js the $ will be unrecognized, and an error will be displayed. This is where the .jslintrc file comes in handy.

**.jslintrc** is *a file you create in each project* that allows you to override jslint defaults. In the case of the JQuery issue mentioned above, I could simply add the predef option like this:

{% highlight javascript %}
{
  "predef" : ["$"]
}
{% endhighlight %}

Another issue is that JSLint defaults to 4 spaces for tab indentation. If you use 2 spaces, like me, JSLINT will issue an error. This is also easily fixed with .jslintrc.

{% highlight javascript %}
{
  "indent" : 2
}
{% endhighlight %}

Check out the JSLint page for a complete list of [customizable options](http://www.jslint.com/lint.html#options).
