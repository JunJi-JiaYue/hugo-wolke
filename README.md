Wolke
===
このテーマは [Re Robust](https://github.com/39e/hugo-rerobust) をベースに作成しました。  

## shortcode
一部 shortcode は公式のものを使用しています。

### Gist
`{{< gist id="gistID" file="file" >}}`

### Twitter
`{{< twitter id >}}`

### YouTube
`{{< youtube id >}}`
`{{< youtube id autoplay="true" >}}`

## シェアボタン
シェアボタンのURLを更新し、非表示を可能です
各シェアボタンを非表示するには以下のようにしてください

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

シェアボタン自体を非表示にするには以下のようにすることで可能です

```toml
[Params]
socialShare = false
```