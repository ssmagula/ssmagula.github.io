[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/ssmagula/ssmagula.github.io)

# Understanding this site

This site is is a place for product management and design case studies and articles by Stefan Smagula. See the site here: [Stefan Smagula Case Studies](https://ssmagula.github.io)

## TODO
- Hookup SASS 'asset pipeline' so I don't have to manually rebuild the css files
- Implement pagination on list of posts
- Figure out way to archive posts by month or quarter?
- Get social media addresses rendered from an include
- Write and design a full-page case study page
- Write more case articles
- More!

## DONE!
- Get Google Analytics installed
- Make modals use data (makes all modals easier to edit)
- Investigage using map as hero image (distracting)
- Implemented a person profile page (used timeline)
- Figure out how to process images automatically (Bootstrap img-relative)

## Credits

This site is made with [Jekyll.rb](jekyllrb.com) and used a Bootstrap theme called Agency as a starting point. It even includes SASS, FontAwesome icons, and occasionally some SVG icons from Noun Project.
    

## Usage
To use this site/blog as the basis for your own, install Jekyll then clone this repository. See more Jekyll how-to links in the "Making this site post" in the blog. Feel free to use this Bootstrap + Jekyll blog site as the basis for your own, but take a look at the TODO's above. It's semi-done.

## Boilerplate notes from the default Jekyll installation (Minima theme)

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


## Development

To set up your environment to develop this theme, run `bundle install`.

To test your theme, run `bundle exec rake preview` and open your browser at `http://localhost:4000/minima/`. This starts a Jekyll server using your theme and the contents of the `example/` directory. As you make modifications to your theme and to the example site, your site will regenerate and you should see the changes in the browser after a refresh.


