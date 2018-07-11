Wolke
===
このテーマは [Re Robust](https://github.com/39e/hugo-rerobust) をベースに作成しました。  

## Features
- Responsive design
- AMP (Accelerated Mobile Pages)
- Google Analytics
- Disqus
- Social Share (Hatena Bookmark, Twitter, Facebook, Google+, Pocket, LINE)
- Lazy Loading Images
- Atom Feed

### Installation
```
cd path/to/
git submodule add https://github.com/39e/hugo-wolke themes/wolke
```

## `config.toml` example
```toml
baseurl = "https://example.com/"
title = "SiteTitle"
theme = "wolke"

googleAnalytics = "UA-XXXXXXXX-XX" # Optional
disqusShortname = "XYW" # Optional

[params]
description = "This is site description"
dateformat = "Jan 2, 2006" # Optional

[params.author]
name = "John Doe"
thumbnail = "img/author.png"
description = "This is author description."
facebook = "XXXX"
twitter = "XXXX"
github = "XXXX"

[outputs]
page = ["HTML", "AMP"] # if you want AMP enable.
```

### Atom Feed の有効化
```toml
[mediaTypes]
[mediaTypes."application/atom"]
suffix = "xml"

[outputFormats.Atom]
mediaType = "application/atom"
baseName = "atom" # generated file = <baseName>.<mediaType."application/atom".suffix> = atom.xml
isPlainText = false

[outputs]
home = ["HTML", "RSS", "ATOM"] # default = ["HTML", "RSS"]
```

上記の内容を追加する必要があります

## shortcode
一部 shortcode は公式のものを使用しています。

### Image
```
{{< img src="images/image.jpg" w="600" h="400" >}}
{{< img src="images/image.jpg" w="600" h="400" caption="Referenced from wikipedia." href="https://en.wikipedia.org/wiki/Lorem_ipsum" >}}
```

### Gist
```
{{< gist id="gistID" file="file" >}}
```

### Twitter
```
{{< twitter id >}}
```

### YouTube
```
{{< youtube id="youtubeID" >}}
{{< youtube id="youtubeID" autoplay="true" >}}
```

## Social Share
シェアボタンのURLを更新し、非表示を可能です。
各シェアボタンを非表示するには以下のようにしてください。

```toml
[Params]
# はてなブックマーク
socialShareHatena = false
# Twitter
socialShareTwitter = false
# Facebook
socialShareFacebook = false
# Google Plus
socialShareGoogleplus = false
# Pocket
socialSharePocket = false
# LINE
socialShareLine = false
```

シェアボタン自体を非表示にするには以下のようにすることで可能です。

```toml
[Params]
socialShare = false
```