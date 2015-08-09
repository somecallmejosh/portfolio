---
title:  "Incrementing a Javascript Array Element"
date:   2014-12-06 12:04:03
main_image: "climb.jpg"
flickr_attribution: Mikel Ortega
flickr_link: https://www.flickr.com/photos/mikelo/13297857634/in/photolist-mg5ZMu-bJ2R52-5NPtGb-bo8pUe-NAZ1v-kCyr2W-qwoUdx-58Voz6-3QrUD-srAss-64bTJ-9wF2S-bmsURi-9gzb95-S3h1k-fqfYNH-7g2y9V-foNrFf-bo8ozc-7g6uAb-cnwPk-inYJSd-8ZY7Uh-7g2xie-39nkZt-eLYtzZ-4VjWjW-4VjrvG-kGQanz-4CHWCm-2aLU2s-c2bjvC-4o7tTh-8qvrQ-4VfjDk-iT5Y4M-j4RWaC-imhdU4-4rggWC-6yP927-bJ4HKB-oZN2uJ-oat4bg-7g6v6C-ipw1Cx-pCNa2t-dhyFHV-fFMk6U-7g6qSu-pazFwn
flickr_license: "https://creativecommons.org/licenses/by-nc-nd/2.0/"
---

Working on another problem in the Udacity Javascript Basics Course. The goal is to increment the last element in an array by one. This assumes the elements in the array are numbers

Here is my solution:

{% highlight javascript %}
var sampleArray = [0,0,7];

var incrementLastArrayElement = function(_array) {
  var newArray = _array;
  var arrLength = _array.length-1,
  getLastElement = _array[arrLength],
  editLastElement = getLastElement+1,
  removeLastElement = _array.pop();
  addEditedElement = _array.push(editLastElement);
  return newArray;
};

console.log(incrementLastArrayElement(sampleArray));

// returns: [0,0,8]
{% endhighlight %}

And the slightly more elegant version presented by Udacity:

{% highlight javascript %}
function incrementLastArrayElement(_array)  {
  var newArray = [];
  newArray = _array.slice(0);
  var lastNumber = newArray.pop();
  newArray.push(lastNumber + 1);
  return newArray;
}
{% endhighlight %}
