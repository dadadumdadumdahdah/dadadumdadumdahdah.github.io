# frozen_string_literal: true

source "https://rubygems.org"

gem "jekyll-theme-chirpy", "~> 7.4", ">= 7.4.1"

gem "html-proofer", "~> 5.0", group: :test

platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.2.0", :platforms => [:mingw, :x64_mingw, :mswin]

# 생성일자 자동 추가
group :jekyll_plugins do
#   gem 'jekyll-feed', '~> 0.12'
  gem 'jekyll-sitemap', '~> 1.4'
  gem 'jekyll-seo-tag', '~> 2.7'
  gem 'jekyll-archives', '~> 2.2'
  gem 'jekyll-compose'  # <--- 이 줄을 추가하세요!
end