---
title:  "Remove Items from DOM with JQuery"
date:   2014-12-30 08:24:10
main_image: "picking.jpg"
flickr_attribution: John
flickr_link: https://www.flickr.com/photos/mtsofan/8108255881/in/photolist-dmuVZc-aw9bLA-aw6ENz-aw6uZz-aw9wJw-aw9gPq-aw6Qja-aw95DW-aw9kBL-aw9dum-aw6rCp-aw6w2B-aw9r3N-aw99uC-aw6FnZ-aw6ppx-aw6Hie-aw9mqb-aw6xQ6-aw6CTp-aw9grS-aw6QGe-aw9y3d-aw6yfc-aw9cTs-aw6spg-aw965S-aw9xj9-aw9at5-aw6yFX-aw6uQX-aw6R66-aw6vdD-aw6Co2-aw9cfj-aw9en3-aw9gbC-aw6RZc-aw9qm7-aw6P6B-aw6LBH-aw6FKZ-aw9cAY-aw97fb-aw6NhB-aw9fvh-aw6zDk-aw6MQT-aw6xBR-au56Jr
flickr_license: "https://creativecommons.org/licenses/by-nc-nd/2.0/"
---

Here, I'm using the JQuery [remove()](http://api.jquery.com/remove/) method to remove all the child `<ul>`'s from all of the `.article-item`'s. There's only one child that this can affect, so don't worry about being ovelry selective.

## HTML
{% highlight html %}
<ul class="article-list">
  <li class="article-item">
    <ul>
      <li>Something</li>
    <ul>
  </li>
  <li> class="article-item">
    <p>Something</p>
  </li>
</ul>
{% endhighlight %}

## JQuery
{% highlight javascript %}
var articleItems, ul;
articleItems = $('.article-item');
ul = articleItems.find("ul");
ul.remove();
});

{% endhighlight %}
