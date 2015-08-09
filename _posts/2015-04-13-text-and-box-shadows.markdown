---
title:  "Text and Box Shadows"
date:   2015-04-13 08:05:48
categories: css
main_image: "cat-shadow.jpg"
flickr_attribution: Marina del Castell
flickr_link: https://www.flickr.com/photos/marinadelcastell/8648355911/in/photolist-ebe5UF-oGateB-edi9EK-eohCuy-jLexS7-nLCze8-p9wJjG-HUXXs-iqVPyz-6NSQmF-bVgABu-q9cags-pKBz7S-pmvEB-3FUhu-3Uoeex-9fMkrw-8urrqx-gQRFS-dzsYSS-gQby3x-sxskv-6WUi3U--7Fb2UH-k5Xwuz-iP1vq8-kSoUAQ-dKYL7-mkqoHM-aoR6j2-rdeFWd-iQWMCr-eGnpBb-ozTc9e-rUY8oL-5gWEiu-6J9PCK-mbcr37-9QL3D5-pDdLP9-2nqi5-oSXczX-pFrPpK-8ZHUCG-4zK6TR-7rLBdR-g9hgky-h8xiKJ-h3pN7D
flickr_license: "https://creativecommons.org/licenses/by/2.0/"
---

I get the feeling text shadows are falling out of favor in the flat design world, but box shadows are pretty common with the release of Material design. So, here we go...

##Text Shadows

Adding drop shadows to text and stuff. Accepts four values:

* **horizontal offset**: How far from the left or right the shadow should fall
* **vertical shadow**: How far from the top or bottom a shadow should fall
* **blur radius**: How much blur the shadow should receive (This is an optional value)
  * If this isn't defined, it will be rendered according to the element's color property.
* **color value**: hex, rgb, rgba, keyword

{% highlight css %}
p {
  text-shadow: 5px 8px 0 #222
  // horizontal 5px
  // vertical 8px
  // blur 0
  // color #222
}
{% endhighlight %}

Check out [http://markdotto.com/playground/3d-text/](http://markdotto.com/playground/3d-text/) for creating a 3d-text effect using multiple text shadows.

## Box Shadows

Pretty similar to text shadow approach. Order of values is exactly the same as the text shadow.

{% highlight css %}
.box {
  box-shadow: 5px 8px 0  #222
  // horizontal 5px
  // vertical 8px
  // blur 0
  // color #222
}
{% endhighlight %}


### Inner Shadow

{% highlight css %}
.box {
  box-shadow: inset 5px 8px 0 #222
  // horizontal 5px
  // vertical 8px
  // blur 0
  // color #222
}
{% endhighlight %}

