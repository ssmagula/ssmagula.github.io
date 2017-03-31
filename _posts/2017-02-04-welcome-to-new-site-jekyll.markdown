---
layout: post
flytitle: Incantations
title:  Notes on the new site
comments: true
dek: Some notes on how this site is assembled in .22 seconds by a series of scripts and codes
date:   2017-02-01 20:27:14 -0600
categories:
author: "Stefan Smagula"
img-large: http://cdn.static-economist.com/sites/default/files/imagecache/full-width/images/print-edition/20170128_STP002_0.jpg
img-small: http://cdn.static-economist.com/sites/default/files/imagecache/200-width/images/print-edition/20170128_STP003_2.jpg
---
YOU WILL FIND this post in your `_posts` directory, if you're managing a Jekyll-backed site. I have my Jekyll server running locally, and it's set up such that every edit I make to this file, or any file, will trigger Jekyll to rebuild or regenerate the site, with the changes I made incorporated. When I first heard about static site generators, I was a bit confused. If this was possible all along, why had we not been using static site generators earlier, was one of my questions. Turns out the answer is: because we didn't really know it was so much better! At least that's how I feel.

This site is hosted using Github Pages, which makes hosting Jekyll sites relatively painless and easy, not to mention very cost-effective.

You can rebuild the site locally in many different ways, before you do:
{% highlight ruby %}
git push -u origin master
{% endhighlight %}
to publish the site to Github.io.

There are many ways to generate the site, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates the site when any file is updated.

To add new posts to your blog, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
