---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
---

/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install ruby
gem install bundler jekyll
jekyll new jekyll
cd jekyll/
jekyll build
jekyll serve
gem install jekyll_pages_api
gem install jekyll-json-feed
gem install jekyll-manager

add on GemFile:
group :jekyll_plugins do
  gem "jekyll_pages_api"
  gem "jekyll-json-feed"
  gem "jekyll-sitemap"
end

bundle install
bundle exec jekyll serve
