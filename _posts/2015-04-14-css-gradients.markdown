---
title:  "CSS Gradients"
date:   2015-04-13 20:05:48
categories: css
main_image: "gradient.jpg"
flickr_attribution: Brynn Tweeddale
flickr_link: https://www.flickr.com/photos/marinadelcastell/8648355911/in/photolist-ebe5UF-oGateB-edi9EK-eohCuy-jLexS7-nLCze8-p9wJjG-HUXXs-iqVPyz-6NSQmF-bVgABu-q9cags-pKBz7S-pmvEB-3FUhu-3Uoeex-9fMkrw-8urrqx-gQRFS-dzsYSS-gQby3x-sxskv-6WUi3U--7Fb2UH-k5Xwuz-iP1vq8-kSoUAQ-dKYL7-mkqoHM-aoR6j2-rdeFWd-iQWMCr-eGnpBb-ozTc9e-rUY8oL-5gWEiu-6J9PCK-mbcr37-9QL3D5-pDdLP9-2nqi5-oSXczX-pFrPpK-8ZHUCG-4zK6TR-7rLBdR-g9hgky-h8xiKJ-h3pN7D
flickr_license: "https://creativecommons.org/licenses/by-sa/2.0/"
---

No more using photoshop sliced repeating images for background gradients. 


## Linear Gradients

{% highlight css %}
/* top to bottom is default */
div {
  background-image: linear-gradient(color1, color2);
}

/* reverse color orders */
div {
  background-image: linear-gradient(to top, color1, color2);
}

/* right to left */
div {
  background-image: linear-gradient(to left, color1, color2);
}

/* Angled (rotates clockwise) */
div {
  background-image: linear-gradient(45deg, color1, color2);
  /* starts at bottom left and ends at top right */
  /* 90deg starts on left, ends on right */
}
{% endhighlight %}

## Radial Gradients

{% highlight css %}
/* an ellipse by default, from center */
div {
  background-image: radial-gradient(color1, color2);
}

/* make it a cricle */
div {
  background-image: radial-gradient(circle, color1, color2);
}

/* change the position using 'at' keyword */
div {
  background-image: radial-gradient(cirlce at top, color1, color2);
  /* positions in top center area */
}
div {
  background-image: radial-gradient(cirlce at top right, color1, color2);
  /* positions in top right area */
}
{% endhighlight %}

## Color Stops

Controls the progression of colors within a gradient.
{% highlight css %}
div {
  background-image: radial-gradient(cirlce at top right, color1 0%, color2 50%, color3 100%);
  /* This is equivalent to the default settings for three color stops. */
}

/* Chang the color stop position values. */
div {
  background-image: radial-gradient(cirlce at top right, color1 20%, color2 60%, color3 120%);
  /* This is equivalent to the default settings for three color stops. */
}
{% endhighlight %}

## Gradient Over a Background Image

The background image at the top is higher on the z-index.

{% highlight css %}
div {
  background: 
    linear-gradient(steelblue, transparent 50%), 
    linear-gradient(to top, white, transparent 90%), 
    url('http://lorempixel.com/1000/300/sports/') top left no-repeat;
}
{% endhighlight %}
