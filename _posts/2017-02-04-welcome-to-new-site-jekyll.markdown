---
layout: post
flytitle: Incantations
title:  Notes on this new site
comments: true
dek: Some notes on how this site is assembled in .22 seconds by a series of scripts and codes
date:   2017-02-01 20:27:14 -0600
categories:
author: "Stefan Smagula"
img-large: http://cdn.static-economist.com/sites/default/files/imagecache/full-width/images/print-edition/20170128_STP002_0.jpg
img-small: http://cdn.static-economist.com/sites/default/files/imagecache/200-width/images/print-edition/20170128_STP003_2.jpg
---
YOU WILL FIND this post in your `_posts` directory, if you're managing a Jekyll-backed site. Here's how Jekyll works: you set up a Jekyll server locally and it watches your files for changes. With each change it will automatically re-generate the entire site, with the changes you just made incorporated. This takes about .22 seconds. What can you do with Jekyll? Well, anything that you can do with Ruby. If you look at the list of blog posts in  `/blog` , or the footer of the home page, there's a bit of ruby code embedded in the HTML which is interpreted by Jekyll, and this code says: for each post in the posts list, show me the 3 most recent articles and then generate a 23 word excerpt and output the hed, dek, and excertp into these HTML tags. 

I found Jekyll's includes and layouts easy to navigate. You put the code for your head, header, and footers in the includes directory, then include them into the layouts you create, for example a  `page` layout. When you create a new instance of a `page` , it uses the layout to determine which head, header, and footer go in there.

When I first heard about static site generators, I was a bit confused. If you can do away with a database connection, latency, and fix security issues in one fell swoop, why don't more bloggy sites use static site generators? Turns out the answer is: because we just needed a little time to figure out how simple it is. At least that's how I feel.

This site is hosted using [Github Pages][github-pages], which makes hosting HTTPS sites relatively painless and easy, not to mention very cost-effective (gratis). The icons are by [FontAwesome][font-awesome] FontAwesome.io and the following icons from [Noun Project][noun-project]
 * Recursive triangles, Created by Bohdan Burmich 
 * Donut chart, created by HLD 
 * Lightbulb, created by ImageCatalog 
The hero image on the home page is a photogram of what looks like pine needles. It is attributed to anonymous, and was created during the late 1800's and is in the [Rijskmuseum collection][rijskmuseum] in Amsterdam.

You can rebuild the site locally in many different ways, before you publish the site with a few keystrokes:
{% highlight ruby %}
git push -u origin master
{% endhighlight %}
Not bad, right?

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

[rijksmuseum]: https://www.rijksmuseum.nl/en/my/collections/183512--stefan-smagula/patterns/objecten#/RP-F-F15045,0
[noun-project]: https://thenounproject.com/
[font-awesome]: http://FontAwesome.io/
[github-pages]: https://github.io/
[jekyll-docs]:  https://jekyllrb.com/docs/home
[jekyll-gh]:    https://github.com/jekyll/jekyll
[jekyll-talk]:  https://talk.jekyllrb.com/
