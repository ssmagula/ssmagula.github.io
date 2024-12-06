source "https://rubygems.org"
ruby RUBY_VERSION

# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!
# Smag 2024: commenting this out to see if it fixes ""cannot load such file -- rexml"
# gem "jekyll", "3.4.0" 

# This is the default theme for new Jekyll sites. You may change this to anything you like.
#gem "minima", "~> 2.0" Smag 2017: disable gem theme

# If you want to use GitHub Pages, remove the "gem "jekyll"" above and
# uncomment the line below. To upgrade, run `bundle update github-pages`.
gem "github-pages", group: :jekyll_plugins

# If you have any plugins, put them here!
group :jekyll_plugins do
   gem "jekyll-feed", "~> 0.6"
   # Smag 2024: adding following gem to fix "cannot load such file -- rexml/parsers/baseparser"
   gem "webrick"
end

# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw, :jruby]

