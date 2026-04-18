# frozen_string_literal: true

source "https://rubygems.org"

# Core Jekyll
gem "jekyll", "~> 4.3"

# Plugins required by Minimal Mistakes
group :jekyll_plugins do
  gem "jekyll-paginate",     "~> 1.1"
  gem "jekyll-sitemap",      "~> 1.4"
  gem "jekyll-gist",         "~> 1.5"
  gem "jekyll-feed",         "~> 0.17"
  gem "jekyll-include-cache","~> 0.2"
  gem "jekyll-seo-tag",      "~> 2.8"
  gem "jekyll-remote-theme", "~> 0.4"
end

gem "html-proofer", "~> 5.0", group: :test

platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.2.0", :platforms => [:mingw, :x64_mingw, :mswin]
gem "webrick", "~> 1.8"
