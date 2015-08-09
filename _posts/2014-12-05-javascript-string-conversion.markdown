---
title:  "Javascript String Conversion"
date:   2014-12-06 12:04:03
main_image: "string.jpg"
flickr_attribution: Lorenzoclick
flickr_link: https://www.flickr.com/photos/lorenzoclick/8579869186/in/photolist-e5b5c5-4sYztE-9NhFQL-4teoz9-6GCDqZ-5rJewh-qitVmE-4Bqy4p-Qsmow-8n62Dd-dJU4rw-9p2kid-4vr7MK-beZ1m4-9QfWNA-4xTDCT-d7iN13-jDhkbT-r9ouA-boTTX-3uSXcf-kF1vtZ-d7iMTU-9dpkbT-bC3ecm-cjj7Wm-9VdLSP-a4DMaZ-2fw6rQ-pPFojJ-pRVg8v-5Rs8pK-oUzURn-dczDW6-a4DMda-tQHLP-eixFK6-9yZkuA-6jTvK6-i2RQqx-7QGk5w-a4GC69-a3JkQ7-oe5uje-7J5AuU-oivcnP-odFwno-diY6hh-5keRVg-7841cD
flickr_license: "https://creativecommons.org/licenses/by-nc-nd/2.0/"
---

The challenge is to use string methods to convert one word into a different word. Here’s my solution:

Convert the string `audacity` to `Udacity`.

Any one of the following methods, combined with the HTML example at the bottom will work.

## JS/JQuery

### Method One

This was my original attempt. It’s basically string concatenation, with a new string of “U” to the beginning.

{% highlight javascript %}
var wordToChange = "audacity";
// slice out "dacity" and concatenate with the letter "U"
var changedWord = "U" + wordToChange.slice(2);
// Use JQuery to find the container in the DOM with a class of 'changed'
// Append changedWord to .changed
$('.changed').append(changedWord);
{% endhighlight %}

### Method Two

I slightly refactored method one here by removing the “U”, and instead treated the string as an array, changing the case on the first character of the desired outcome, and then concatenated it with the rest of the original string.

{% highlight javascript %}
var wordToChange = "audacity"
wordToChange = wordToChange[1].toUpperCase() + wordToChange.slice(2);
$('.changed').append(wordToChange);
{% endhighlight %}

### Method Three

This is similar to Udacity’s recommend solution, where they used a function. It’s very similar to my refactored approach above.

{% highlight javascript %}
var wordToChange = "audacity"
var changedWord = function(wordToChange) {
  wordToChange = wordToChange[1].toUpperCase() + wordToChange.slice(2);
  return wordToChange;
};
$('.changed').append(changedWord(wordToChange);
{% endhighlight %}

## The HTML

All of the methods above append the result to the DOM. So, by adding this in the HTML, the result will be displayed in the web page.

`<div class="changed"></div>`

{% highlight javascript %}

{% endhighlight %}
