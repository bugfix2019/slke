# Sri Lanka Knowledge Exchange

## Development

Install dependencies

```
bundle install
```

Clear up dependency issues

```
bundle update
```

Run Jekyll site

```
bundle exec jekyll serve
bundle exec jekyll build
```

If changes are not shown, kill processes on port 4000
```
netstat -ano | findstr :4000

taskkill //PID "PUT_YOUR_PID_HERE" //F
e.g. taskkill //PID 11752 //F
```

## Important URLs

- Guide for Minimal Mistakes Theme
https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/

- Demo Site of Minimal Mistakes Theme
https://mmistakes.github.io/minimal-mistakes/

- Add Google Adsense
https://github.com/mmistakes/minimal-mistakes/issues/404,
https://github.com/mmistakes/minimal-mistakes/blob/master/docs/_layouts/default.html#L24-L34,
https://github.com/mmistakes/minimal-mistakes/issues/1923,

- Jekyll Cheat Sheet
https://devhints.io/jekyll

- Syntax Styles
https://mmistakes.github.io/minimal-mistakes/markup-syntax-highlighting/
https://mmistakes.github.io/minimal-mistakes/docs/stylesheets/#syntax-highlighting

- Layout: Post with Table of Contents
https://mmistakes.github.io/minimal-mistakes/layout-table-of-contents-post/

- Custom Sidebar (override author profile sidebar)
https://mmistakes.github.io/minimal-mistakes/layout-sidebar-custom/ 
https://mmistakes.github.io/minimal-mistakes/layout-sidebar-nav-list/

- Wide Layout
https://mmistakes.github.io/minimal-mistakes/markup-text-readability-wide-page/

- Layout: Header Overlay with Background Fill
https://mmistakes.github.io/minimal-mistakes/layout/uncategorized/layout-header-overlay-color/

----------------------------------------------------------
## Theme Installation

Copy-Paste the theme files to project root.

Remove unnecessary files and directories:
```
.editorconfig
.gitattributes
.github
/docs
/test
CHANGELOG.md
minimal-mistakes-jekyll.gemspec
README.md
screenshot-layouts.png
screenshot.png
```

Update `Gemfile`

```
source "https://rubygems.org"

# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!

# gem "github-pages", group: :jekyll_plugins

# To upgrade, run `bundle update`.

# gem "jekyll"
gem "github-pages"
gem "minimal-mistakes-jekyll"

# The following plugins are automatically loaded by the theme-gem:
#   gem "jekyll-paginate"
#   gem "jekyll-sitemap"
#   gem "jekyll-gist"
#   gem "jekyll-feed"
#   gem "jemoji"
#   gem "jekyll-data"
#   gem "jekyll-include-cache"
#
# If you have any other plugins, put them here!
group :jekyll_plugins do
end
```

To install latest unreleased version of theme: add 

```
gem "minimal-mistakes-jekyll", :github => "mmistakes/minimal-mistakes"
```