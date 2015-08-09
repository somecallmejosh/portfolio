---
title:  "Lexical Scope"
date:   2014-12-30 23:41:33
main_image: "dolls.jpg"
flickr_attribution: Shaheer Shahid
flickr_link: https://www.flickr.com/photos/shaheershahid/3635625771/in/photolist-6xgwSX-dEGZaX-6bNpQx-6HDp2q-8pYfZe-qKjBH-gQuSx-GAipG-c6BTDQ-HWezW-4u4LVB-6bSyUL-AkjL-5Vojrc-4LRAm9-g89y59-HWezQ-7V5K1z-21f87-mqruod-5tVJB9-4imysc-4imyuv-9d29ga--9ToVL-7MmRy-oRjFJF-bvTM3k-9Tp4X-e7qJh-e7pZr-e7pck-p6LRtJ-5W1o5D-pWRCf-8QEhu-6BVwpy-9d29e4-7DbeTk-5xJsy9-jJ2cq-9JW8yz-bEiYBV-e7qcV-8jRFUn-8XTF9B-4ShiaA-dF36vG-e7qqc
flickr_license: "https://creativecommons.org/licenses/by-nc-nd/2.0/"
---

*In simple programs with no functions at all, there is only one scope — Global Scope.* [[ref]](https://www.udacity.com/course/viewer#!/c-ud015-nd/l-2593668697/m-2541189052). **Lexical scope** simply defines the locations from where variables are accessible. Variables can be global, or enclosed in a function. There's other regions within a program a variable can be declared, but we'll stick with global and function enclosed versions for now. If I have only one single variable in a javascript program, like this:

{% highlight javascript %}
var hero = aHero();
{% endhighlight %}

`hero` is said to be in the global scope. So, it's lexical scope is global. That means I can access that variable anywhere within the program. It's accessible everywhere within the program.

Some variables are not global. They are declared within functions. For instance:

{% highlight javascript %}
var heroAction = function(){
  var jump = "high";
};

console.log(jump);
// Returns undefined because it's not in the global scope.
{% endhighlight %}

The lexical scope for `jump` is within the `heroAction` function. I cannot access the variable in the global scope, but **only from within the `heroAction` function**.  Every inner level can access variables from outer layers, but the opposite is not true. Variables defined inside a function, for instance, are not accessible outside of that function.

## Considerations

### Variable Declarations Within Functions

Below, you'll notice a variable is being defined within a function. However, not using the keyword `var` causes that variable to move to the Global Scope. It's not good practice to do this.

{% highlight javascript %}
var heroAction = function(){
  jump = "high";
};

console.log(jump);
// Returns "high"
// I'm not able to reproduce this behavior in the Google Chrome browser, however.
{% endhighlight %}

### Curly Braces

Curly braces `{...block info...}` in Javascript are not necessarily relevant for scoping. Blocks on looping constructs do not create new scope. Blocks in functions, however, do.
