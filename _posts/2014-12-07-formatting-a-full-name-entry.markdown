---
title:  "Formatting a Full Name Entry"
date:   2014-12-07 12:04:03
main_image: "name.jpg"
flickr_attribution: Why Tuesday
flickr_link: https://www.flickr.com/photos/whytuesday/2637517202/in/photolist-524XYw-4G8oR4-9Wrm1z-fzxoGa-aPoRP-4WdNNJ-4sHV8t-51Yhom-3mhYX-3mhYW-3mhYV-5CzuCz-4CWFSN-8gvNct-bQTz7-mCrFbz-i1zUCQ-5Ajcm8-5Lh8uk-6AXWYR-25t6wp-6CsJDt-5ytU2a-m64wX-m68Wb-7ouFEA-5x5VXx-29pR7U-8gz4YS-Kh1Zp-T5rqn-SXGB4-4bqWaq-6uwcAK-efJfzA-7oNRwZ-7oSJ6b-7oSHum-8ZYZBM-5AzRBQ-6P682V-8ZYZuB-6bVDz9-abgUA1-fqVwmr-5LhexT-7JnGoX-efHonJ-efHoid-efHoE7
flickr_license: "https://creativecommons.org/licenses/by-nc-nd/2.0/"
---

Let’s imagine we have a form that captures fullName in a single text field. We’ll assume the person entering their name has only two names, a first name and a last name. In an ideal world, they’d enter their name in a proper format, such as “John Doe.” However, the possibility exists that someone may enter it with different formatting, such as “john doe”, or “john DoE”, or…

We can use the following code to convert the full name to ensure proper formatting:

## Method One

{% highlight javascript %}
// captured from a form field, or a prompt
var fullName = "joHn dOE";

// Return the index of the single space character that separates the names
var spacer = fullName.indexOf(" ");

// Find first name
var firstName = fullName.slice(0, fullName);

// Find last name
var lastName = fullName.slice(fullName + 1);

// Capitalize first letter of each name
firstName = firstName[0].toUpperCase + firstName.slice(1).toLowerCase();
lastName = lastName[0].toUpperCase = lastName.slice(1).toLowerCase();

// Return properly formatted full name
var finalName = firstName + " " lastName;
{% endhighlight %}

## Method Two

**Refactored**, using split() and join()

The method above definitely works. There’s a shorter way using the split() method. Rather than searching for the index of the “separator” character, split() will do the work for us. Then we can use the join() method to glue the names back together.

{% highlight javascript %}
var fullName = "jOHN dOe";
var names = fullName.split(" ");

// Convert First Name
names[0] = names[0].slice(0,1).toUpperCase() + names[0].slice(1).toLowerCase();

// Convert Last Name
names[1] = names[1].slice(0,1).toUpperCase() + names[1].slice(1).toLowerCase();

var finalName = names.join(" ");
{% endhighlight %}

Pretty cool, right?
