---
title:  "REMs and EMs Conversions"
date:   2015-04-12 13:05:48
categories: css
main_image: "ruler.jpg"
flickr_attribution: Scott Akerman
flickr_link: https://www.flickr.com/photos/sterlic/4299631538/in/photolist-C95Ys-oRrdMA-7xWJEf-mKQ2JR-4YkJYo-7xWK7u-77XW6S-e3uy6S-gH1GA-7vBn9x-oRcnwr-5P4Gpi-4YkJMJ-e4ZTnB-cEU9ny-3r7M89-3p8Rg4-6SxgYM-qCqJ6h-om6w98-7PH6S6-88FRg-68Bhi1-4LxGvE-S6RvQ-9woxW3-cEU9S9-dDMbZA-cEUa29-br86US-9BQuMp-9Ca9XB-aTAMvF-5UL6oh-doNnVF-dgCrmM-efeYFA-7nvXkn-8MDfSg-e3oPPZ-cEU9Ho-55XoaG-bpQYz8-4zNN3p-d2vV6C-2dhjjB-dcrHum-7wzTDN-4zpege-dGcJ7d
flickr_license: "https://creativecommons.org/licenses/by/2.0/"
---

Talking about simple relative font sizing in this post. Gonna take a look at REMs and EMs. Let's look at the similarites, differences and how to convert them to pixels.

##EM Units

EM Units are calculated based on a parent element's font size.

{% highlight css %}
html {font-size: 16px;} /* This is the context value */
html p {font-size: 1em;} /* == 16px */
html p {font-size: 1.5em} /* == 24px */
{% endhighlight %}

If the parent is 16px, then 1em is the equivalent size.


###Converting `px` to `em`

Convert 26px with a context of 16px

formula: `desired px value / parent context = em value`

26px/16px = 1.625em

###EM Unit Compounding problem

If nested, the context changes.

{% highlight css %}
.header {font-size: 2em;}
.header p {font-size: 1.625em} /* now based on the context of header.  */
{% endhighlight %}

original context = 16px

new context = 16px * 2 (32px)

.header p = 52px, as opposed to 16px which we may have thought it would.


##REM Units

REM stands for **R**oot *EM* Unit

REMs help resolve the compounding issues of EM Units because they are sized relative to the root element (html) of the page. They're not affected by inheritance like EM Units.

`.header p (font-size: 1.625rem}`

now equals 26px

Here's a sample:

<p class="sassmeister" data-gist-id="a06e5effebc8fd039985" data-height="550" data-theme="tomorrow"><a href="http://sassmeister.com/gist/a06e5effebc8fd039985">Play with this gist on SassMeister.</a></p><script src="http://cdn.sassmeister.com/js/embed.js" async></script>
