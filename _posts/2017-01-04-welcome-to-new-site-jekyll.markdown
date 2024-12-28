---
layout: post
flytitle: Incantations
title:  Making this site
comments: true
dek: Some notes on how this site is assembled in .22 seconds by a series of scripts and codes
date:   2017-04-02 09:27:14 -0600
categories:
author: "Stefan Smagula"
img-large: http://cdn.static-economist.com/sites/default/files/imagecache/full-width/images/print-edition/20170128_STP002_0.jpg
img-small: http://cdn.static-economist.com/sites/default/files/imagecache/200-width/images/print-edition/20170128_STP003_2.jpg
---
YOU WILL FIND this post in your `_posts` directory, if you're managing a Jekyll site. Jekyll is a static site generator, written in Ruby. Here's how it works: you install Jekyll locally: 
{% highlight ruby %}
~ $ gem install jekyll bundler
{% endhighlight %}

and you generate the scaffolding for a new site with a brief incantation like this: 
{% highlight ruby %}
~ $ jekyll new my-new-site-name
{% endhighlight %}

Then you simply move to the site directory you just created 
{% highlight ruby %}
~ $ cd my-new-site-name
{% endhighlight %}
and then from inside that directory, you run the Jekyll server 
{% highlight ruby %}
~/my-new-site-name $ bundle exec jekyll serve --watch
{% endhighlight %}
Now that the server is 'watching' your site for changes, as you add code and content, Jekyll automatically re-generates the entire site. In my case, with just a few pages, the process takes .22 seconds. 

Then you push the site to a git repository like [Github][github], and publish it via Github Pages.

#### CREATE A NEW BRANCH
Create a new branch with git
{% highlight ruby %}
git branch <new-branch-name> 
{% endhighlight %}
or checkout an existing branch
{% highlight ruby %}
git checkout -b <new-branch-name> 
{% endhighlight %}

#### REBUILD AND PUBLISH
You can rebuild the site locally in many different ways, but using the --watch flag is simple. 
{% highlight ruby %}
bundle exec jekyll serve --watch
{% endhighlight %}
Now, as you make edits, the site will regenerate, and you can preview the changes in a new browser tab that is pointing at the right ports (in a Github Codespace which uses VS Code, just go to the Ports tab and click on the globe icon to open a preview of the site)

To add new posts to your blog, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext`and includes the necessary front matter.
Then make edits to files in the `_posts` directory. When you are done, quit the jekyll server with `ctrl-c`, and then add all the changes to git's staging area:
{% highlight ruby %}
git add .
{% endhighlight %}
Now you are ready to commit the changes with a message describing what changed
{% highlight ruby %}
git commit -m "Your commit message" 
{% endhighlight %}
Then push your branch to the remote repo
{% highlight ruby %}
git push origin <new-branch-name> 
{% endhighlight %}
Finally, checkout master, pull master to make sure master is up to data, and then merge and push:
{% highlight ruby %}
git checkout master
git pull origin master  # Ensure master is up-to-date
git merge <new-branch-name>
git push -u origin master
{% endhighlight %}
Your site will be updated in a minute or so. If you want to delete the branch you can
{% highlight ruby %}
git branch -d <new-branch-name>
{% endhighlight %}


#### WHY JEKYLL?
What can you do with Jekyll? Well, pretty much anything that you can do with Ruby. If you're like me, and eager to learn more Ruby, then Jekyll is a great way to ease into things. Take a look at the list of blog posts in `/blog` (or the footer of the home page), under the hood there's a bit of embedded Ruby in the HTML and this Ruby says: make a list of all the blog articles, discard all but the most recent four posts, then create a 23-word excerpt for each, and output the hed, dek, small image, and excerpt into these HTML tags here. The hed, dek, etc. are all defined in the front matter of the markdown file you use to create the post. 'Front matter' sound confusing? Just open the sample posts that are baked into the default new site. It'll make instant sense. They're just variables that you can refer to elsewhere.

I found Jekyll's includes and layouts easy to navigate. You put reusable code for the head, header, and footers in the includes directory, then include them into layouts you create, for example a  `page` layout. When you create a new instance of a `page`, it knows that a  `page` is just a slight variation on the `default` layout.

Because there's no database in the backend, there's reduced complexity, increased security, and each page is much snappier to load.

When I first heard about static site generators, I was a bit confused. If this were possible, why aren't more bloggy sites using static site generators? Turns out the answer is: because we just needed a little time to figure out how simple it is. At least that's how I feel.

#### CREDITS
This site is hosted using [Github Pages][github-pages], which makes hosting HTTPS sites relatively painless and easy, not to mention very cost-effective (gratis). I used the Bootstrap Agency theme for its animated fixed nav bar and nice timeline CSS. All icons are by [FontAwesome][font-awesome], and from time to time I use the following icons from the [Noun Project][noun-project]
 * Recursive triangles, Created by Bohdan Burmich 
 * Donut chart, created by HLD 
 * Lightbulb, created by ImageCatalog 
 
The full-bleed image at the top of the site is a photogram of pine needles. I chose this image because it reveals the rhythm, inner structure of something simple, something we take for granted. It is "Dennenaalden, anonymous, 1840 - 1845" and is part of the [Rijskmuseum collection][rijksmuseum] in Amsterdam.

#### Jekyll also offers support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[github]: https://github.com/
[rijksmuseum]:  https://www.rijksmuseum.nl/en/my/collections/183512--stefan-smagula/patterns/objecten#/RP-F-F15045,0
[noun-project]: https://thenounproject.com/
[font-awesome]: http://FontAwesome.io/
[github-pages]: https://github.io/
[jekyll-docs]:  https://jekyllrb.com/docs/home
[jekyll-gh]:    https://github.com/jekyll/jekyll
[jekyll-talk]:  https://talk.jekyllrb.com/
