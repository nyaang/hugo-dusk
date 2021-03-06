Simple minimalistic dark theme for [Hugo](https://gohugo.io/).

![screenshot](https://github.com/gyorb/hugo-dusk/blob/master/images/tn.png "screenshot")

## Features

* Responsive minimalistic design
* Configurable theme colors
* Syntax highlight with builtin [Chroma](http://gohugo.io/content-management/syntax-highlighting/)
* [OpenGraph](http://ogp.me/), [Twitter cards](https://dev.twitter.com/cards/overview) support
* [Disqus](https://disqus.com/) comments support
* [Google analytics](https://www.google.com/analytics/) (async)
* Configrable pagination for posts
* Lazy menu
* Custom 404 page

## Installation

~~~sh
$ mkdir themes
$ cd themes
$ git clone https://github.com/gyorb/hugo-dusk
~~~

## Configuration

My configuration:

~~~~toml
baseurl = "/"
title = "Yang's Blog"
copyright = "2018, Yang."
canonifyurls = true
hasCJKLanguage=true
summaryLength=20
languageCode = "zh-cn"
paginate = 3
theme = "hugo-dusk"

googleAnalytics = ""
disqusShortname = "yang-cat"

[author]
  name = "Yang"

SectionPagesMenu = "main"

# use Chroma for syntax highlight
pygmentsStyle = "native" # other dark style options: vim, fruity, monokai
# enable syntax highlight for code blocks
pygmentsCodeFences = true

[[menu.main]]
  name = "Posts"
  weight = -120
  identifier = "post"
  url = "/post/"

[[menu.main]]
  name = "Tags"
  weight = -110
  identifier = "tag"
  url = "/tags/"

[params.meta]
  keywords = "blog, tech"
  description = "Personal blog."

[params]
  github = "nyaang"
  #gitlab = "gitlab id"
  #twitter = "twitter id"
  #linkedin = "linkedin id"
  #email = "myemail"

[params.colors]
  # hugo-dusk colors
  background = "#101010" # background color for the site
  main = "#99cc66"
  text = "#dbdbdb"
  code-quote-bg = "#1D1F21" # background color for quotes and code blocks
  copyright = "#404040" # copyright text color
~~~~
