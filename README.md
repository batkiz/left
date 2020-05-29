# left

`left` is a hugo theme forked from [KeepIt](https://github.com/Fastbyte01/KeepIt) (which is based on [LeaveIt](https://github.com/liuzc/LeaveIt)).

take a quick look [here](https://blog.batkiz.com)

## difference

this theme has lots of enhancement on LeaveIt, e.g.
* auto dark mode (unfortunately we don't have manual option now)
* mathjax support
* better code highlighting (auto change light/dark based on the theme!)
* article heading anchors
* etc.

### code highlight
be sure to add
```toml
[markup]
  [markup.highlight]
    codeFences = false
```
to your config file or you will get an annoying code block

### mathjax
if you want use mathjax, please add
```toml
mathjax = true
```
both to your site config file and your article file frontmatters.(the example is `toml` code, use yaml or json based on your own config file/article frontmatters)

## example config

an example config file is like this:

```toml
baseURL = "https://blog.example.com/"
languageCode = "zh-cn"
title = "example blog"

theme = "left"

hasCJKLanguage = true # if your lang is not Chinese, Japanese or Korean, pls comment this line
paginate = 12
enableEmoji = true
enableRobotsTXT = true
googleAnalytics = ""
disqusShortname = "yourdiscussshortname"

[sitemap]
    changefreq = "monthly"
    filename = "sitemap.xml"
    priority = 0.5

[Permalinks]
    posts = "/posts/:year/:filename/"

# disable condeFences to use theme code highlight
# or this will give u an annoying code block background color
[markup]
  [markup.highlight]
    codeFences = false

[menu]
  [[menu.main]]
    name = "Posts"
    url = "/posts/"
    weight = 1

  [[menu.main]]
    name = "Tags"
    url = "/tags/"
    weight = 3

  [[menu.main]]
    name = "About"
    url = "/about"
    weight = 4

  [[menu.main]]
    name = "RSS"
    url = "/atom.xml"
    weight = 5

[params]
    since = 2020
    author = "batkiz"               # Author's name
    subtitle = ""
    home_mode = "" # post or other

    mathjax = true

    google_verification = ""
    bing_verification = ""
    yandex_verification = ""
    pinterest_verification = ""
    baidu_verification = ""

    avatar = "" #comment it to use gravatar
    socialShare = false

    description = "" # site description
    keywords = "" # site keywords

    license= '如无特殊声明，本博客文章均以 <a href="https://creativecommons.org/licenses/by-nc-sa/4.0/" target="_blank">CC BY-NC-SA 4.0</a> 协议发布'

[params.gravatar]
    #email = "example@gmail.com"   #uncomment and insert your email address to use gravatar


[params.social]
    #GitHub = "xxxx"
    #Linkedin = "xxxx"
    #Twitter = "xxxx"
    #Instagram = "xxxx"
    #Email   = "i@xxxx.com"
    #Facebook = "xxxx"
    #Telegram = "xxxx"
    #Medium = "xxxx"
    #Gitlab = "xxxx"
    #Youtubelegacy = "xxxx"
    #Youtubecustom = "xxxx"
    #Youtubechannel = "xxxx"
    #Tumblr ="xxxx"
    #Quora = "xxxx"
    #Keybase = "xxxx"
    #Pinterest = "xxxx"
    #Reddit = "xxxx"
    #Codepen = "xxxx"
    #Bitbucket = "xxxx"
    #Stackoverflow = "xxxxx"
    #Weibo = "xxxx"
    #Odnoklassniki = "xxxx"
    #VKontakte = "xxxx"
    #Flickr = "xxxx"
    #Xing = "xxxx"
    #Snapchat = "xxxx"
    #Soundcloud = "xxxx"
    #Spotify = "xxxx"
    #Bandcamp = "xxxx"
    #Paypal = "xxxx"
    #Fivehundredpx = "xxxx"
    #Mix = "xxxx"
    #Goodreads = "xxxx"
    #Lastfm = "xxxx"
    #Foursquare = "xxxx"
    #Hackernews = "xxxx"
    #Kickstarter = "xxxx"
    #Patreon = "xxxx"
    #Steam = "xxxx"
    #Twitch = "xxxx"
    #Strava = "xxxx"
    #Skype = "xxxx"
    #Whatsapp = "xxxx"
    #Zhihu = "xxxx"
    #Douban = "xxxx"
    #Angellist = "xxxx"
    #Slidershare = "xxxx"
    #Jsfiddle = "xxxx"
    #Deviantart = "xxxx"
    #Behance = "xxxx"
    #Dribble = "xxxx"
    #Wordpress = "xxxx"
    #Vine = "xxxx"
    #Googlescholar = "xxxx"
    #Researchgate = "xxxx"
    #Mastodon = "xxxx"
    #Thingiverse = "xxxx"

[params.share]
    #Twitter = true
    #Facebook = true
    #Reddit = true
    #Linkedin = true
    #Pinterest = true
    #HackerNews = true
    #Mix = true
    #Tumblr = true
    #VKontakte = true
    #Douban = true
    #Weibo = true

# for RSS
copyright = "This work is licensed under a Creative Commons Attribution-NonCommercial 4.0 International License."
defaultContentLanguage = "en"

[outputs]
    home = [ "Atom", "HTML" ]

[outputFormats.Atom]
    mediatype = "application/rss"
    baseName = "atom"

[author]
    name = "xxxx"

  [params.publisher]
    name = "xxxx"

  [params.publisher.logo]
    url = "logo.png"
    width = 127
    height = 40

  [params.logo]
    url = "logo.png"
    width = 127
    height = 40

  [params.image]
    url = "cover.png"
    width = 800
    height = 600
    
# comments

[params.gitalk]
    owner = ""       # Your GitHub ID       
    repo = ""        # The repo to store comments    
    clientId = ""    # Your client ID      
    clientSecret = "" # Your client secret

[params.valine]
    enable = false
    appId = 'your appId'
    appKey = 'your appKey'
    notify = false  # mail notifier , https://github.com/xCss/Valine/wiki
    verify = false # Verification code
    avatar = 'mm'
    placeholder = 'your comments ...'
    visitor = true

[params.utterances]       # https://utteranc.es/
    owner = ""              # Your GitHub ID
    repo = ""               # The repo to store comments

[params.gitment]          # Gitment is a comment system based on GitHub issues. see https://github.com/imsun/gitment
    owner = ""              # Your GitHub ID
    repo = ""               # The repo to store comments
    clientId = ""           # Your client ID
    clientSecret = ""       # Your client secret
```