# Understanding this site

This site is based on a Bootstrap theme called Agency. It contains placeholder content, images, text, etc. I took the default theme for Jekyll, called Minima, and merged that with a new (my first) Jekyll theme. I did it by running `jekyll new` and then looking at the structure of the includes, layouts, posts, and pages, and seeing how assets like CSS and JS need to be included. It was daunting at first, but quickly made sense as I fiddled with it. I recommend this approach (Bootstrap theme, then merge it with Jekyll theme, then develop a Jekyll site)
to others, like me, who want speedy and easy to maintain sites with changing content. —Stefan Smagula

Here's what I started with, which is nothing like what I ended up with! ![minima theme preview](/screenshot.png)

## TODO
- Implement pagination on the /news.html list of articles
- Figure out a way to automatically archive articles by month or quarter
- Get Google Analytics installed
- Get social media addresses rendered from an include
- Design and implement person profile pages
- Improve the station details modal
- Get real data for station details modals
- Add all stations to the map
- Investigage using map as hero image
- Investigate dynamic geocoding of station addresses
- Figure out how to process images automatically (if needed?)
- More!


## Description

This is a marketing site that is powered by [Jekyll.rb](jekyllrb.com) and Bootstrap.
    

## Usage
I don't intend for anyone to use or install this site or theme, I'm just parking it here for now. All rights reserved. Copyright 2017 etc.

### Customization of the default Jekyll theme (Minima)

To override the default structure and style of minima, simply create the concerned directory at the root of your site, copy the file you wish to customize to that directory, and then edit the file.
e.g., to override the [`_includes/head.html `](_includes/head.html) file to specify a custom style path, create an `_includes` directory, copy `_includes/head.html` from minima gem folder to `<yoursite>/_includes` and start editing that file.

The site's default CSS has now moved to a new place within the gem itself, [`assets/main.scss`](assets/main.scss). To **override the default CSS**, the file has to exist at your site source. Do either of the following:
- Create a new instance of `main.scss` at site source.
  - Create a new file `main.scss` at `<your-site>/assets/`
  - Add the frontmatter dashes, and
  - Add `@import "minima";`, to `<your-site>/assets/main.scss`
  - Add your custom CSS.
- Download the file from this repo
  - Create  a new file `main.scss` at `<your-site>/assets/`
  - Copy the contents at [assets/main.scss](assets/main.scss) onto the `main.scss` you just created, and edit away!
- Copy directly from Minima 2.0 gem
  - Go to your local minima gem installation directory ( run `bundle show minima` to get the path to it ).
  - Copy the `assets/` folder from there into the root of `<your-site>`
  - Change whatever values you want, inside `<your-site>/assets/main.scss`

--

### Enabling comments (via Disqus)

I have not tried this, but intend to: 
Optionally, if you have a Disqus account, you can tell Jekyll to use it to show a comments section below each post.

To enable it, add the following lines to your Jekyll site:

```yaml
  disqus:
    shortname: my_disqus_shortname
```

You can find out more about Disqus' shortnames [here](https://help.disqus.com/customer/portal/articles/466208).

Comments are enabled by default and will only appear in production, i.e., `JEKYLL_ENV=production`

If you don't want to display comments for a particular post you can disable them by adding `comments: false` to that post's YAML Front Matter.

--

### Enabling Google Analytics

Something else I will explore next: 
To enable Google Anaytics, add the following lines to your Jekyll site:

```yaml
  google_analytics: UA-NNNNNNNN-N
```

Google Analytics will only appear in production, i.e., `JEKYLL_ENV=production`

## Contributing

Bug reports and pull requests that relate to the Minima theme (the default) are welcome on GitHub at https://github.com/jekyll/minima. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Development

To set up your environment to develop this theme, run `bundle install`.

To test your theme, run `bundle exec rake preview` and open your browser at `http://localhost:4000/minima/`. This starts a Jekyll server using your theme and the contents of the `example/` directory. As you make modifications to your theme and to the example site, your site will regenerate and you should see the changes in the browser after a refresh.

## License

This theme and site are not public domain.
