---
layout: post
flytitle: Incantations
title:  Notes on this new site
comments: true
dek: Some notes on how this site is assembled in .22 seconds by a series of scripts and codes
date:   2017-04-01 09:27:14 -0600
categories:
author: "Stefan Smagula"
img-large: http://cdn.static-economist.com/sites/default/files/imagecache/full-width/images/print-edition/20170128_STP002_0.jpg
img-small: http://cdn.static-economist.com/sites/default/files/imagecache/200-width/images/print-edition/20170128_STP003_2.jpg
---
YOU WILL FIND this post in your `_posts` directory, if you're managing a Jekyll-backed site. Jekyll is a static site generator, written in Ruby. Here's how it works: you install Jekyll locally and you generate the scaffolding for a new site with a brief incantation. As you add code and content, Jekyll automatically re-generates the entire site. This process takes .22 seconds. What can you do with Jekyll? Well, pretty much anything that you can do with Ruby. If you look at the list of blog posts in  `/blog` , or the footer of the home page, under the hood there's a bit of embedded Ruby in the HTML and this code says: show me the 3 most recent articles and then create a 23-word excerpt for each, and output the hed, dek, small image, and excerpt into these HTML tags. 

I found Jekyll's includes and layouts easy to navigate. You put reusable code for the head, header, and footers in the includes directory, then include them into layouts you create, for example a  `page` layout. When you create a new instance of a `page`, it knows that a  `page` is just a slight variation on the `default` layout.

When I first heard about static site generators, I was a bit confused. If this were possible, why aren't more bloggy sites using static site generators? Turns out the answer is: because we just needed a little time to figure out how simple it is. At least that's how I feel.

This site is hosted using [Github Pages][github-pages], which makes hosting HTTPS sites relatively painless and easy, not to mention very cost-effective (gratis). I used the Bootstrap Agency theme for its animated fixed nav bar and nice timeline CSS. All icons are by [FontAwesome][font-awesome] FontAwesome.io except for the following icons from the [Noun Project][noun-project]
 * Recursive triangles, Created by Bohdan Burmich 
 * Donut chart, created by HLD 
 * Lightbulb, created by ImageCatalog 
 
The full-bleed image at the top of the site is a photogram of pine needles. I chose this image because it reveals the inner structure of something simple, something we take for granted. It is attributed to anonymous, was created during the late 1800's, and is currently part of the [Rijskmuseum collection][rijksmuseum] in Amsterdam.

You can rebuild the site locally in many different ways, before you publish the entire site with a new incantation:
{% highlight ruby %}
git push -u origin master
{% endhighlight %}
Simple, right? 

There are many ways to generate the site, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates the site when any file is updated.

To add new posts to your blog, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter.  

Jekyll also offers support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[rijksmuseum]:  https://www.rijksmuseum.nl/en/my/collections/183512--stefan-smagula/patterns/objecten#/RP-F-F15045,0
[noun-project]: https://thenounproject.com/
[font-awesome]: http://FontAwesome.io/
[github-pages]: https://github.io/
[jekyll-docs]:  https://jekyllrb.com/docs/home
[jekyll-gh]:    https://github.com/jekyll/jekyll
[jekyll-talk]:  https://talk.jekyllrb.com/
