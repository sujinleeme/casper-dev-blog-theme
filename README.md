# Customized ghost casper theme for developer's blog

> Inspired from Hungys's [CasperS](https://github.com/hungys/CasperS)

This repo is customized casper theme for my ghost dev blog. Currently, it lives on [sujinlee.me](https://sujinlee.me/).

- [Casper 3](https://github.com/TryGhost/Casper)
- Works with Ghost 3+
- Google Analytics integration
- Disqus integration (comments, comment count)
- Prism-powered syntax highlight
- KaTex
- Social links with Simple Icons integration (TBD)
- LightMode / DarkMode

## How to install theme in your live ghost

- Download this repo as `zip` file.
- Go to your desgin panel in ghost admin page (https://<ghost-blog-url>/ghost/#/settings/design)
- Click `Upload a theme` button and upload zip file.
- Activate new theme.
- Go to code injection panel. (https://<ghost-blog-url>/ghost/#/settings/code-injection)
- Update google analytics variable in **Site Header** code block.

```html
<script>
  var ga_id = "your_google_id"
</script>
```

- Update social links and google analytics variables in **Site Footer** code block.
  - Social icons : facebook, flickr, github, gmail, googleplus', instagram, line, linkedin, messenger, microsoftoutlook, plurk, sinaweibo, skype, snapchat, stackoverflow, telegram, twitter, wechat, whatsapp

```html
<script>
  var social_link = {
    linkedin: "https://www.linkedin.com/in/username",
    github: "https://github.com/username",
    medium: "https://medium.com/@userid"
  }
</script>
```

- Update your disqus shortname in **Site Footer**.

```html
<script>
  var disqus_shortname = "sujinlee"
</script>
```

## Disqus configuration

- Create your disqus website.
- [Customize comment count link text.](https://help.disqus.com/en/articles/1717274-adding-comment-count-links-to-your-home-page)

## Katex usage

- Use a pair of single(`$`)/double(`$$`) dollar sign as formula delimiter.

![katex](https://sujinlee.me/content/images/2019/09/katex.png)

## How to customize casper theme

- 한국어 가이드 (Korean)
  - [뚝딱뚝딱 Ghost로 기술 블로그 만들기 - (1) 설치와 호스팅](https://sujinlee.me/how-to-build-ghost-blog/)
  - [뚝딱뚝딱 Ghost로 기술 블로그 만들기 - (2) 블로그 테마 수정하기](https://sujinlee.me/how-to-build-ghost-blog-2/)

* Install ghost locally as following [official setup guide doc](https://ghost.org/docs/install/local/).
* Clone or download repo and put them in `content/themes/` folder under your Ghost installation.

```
$ cd /[your-ghost-root-directory]
$ git clone https://github.com/sujinleeme/casper-dev-blog-theme.git content/themes/[theme-name]
```

- Run `ghost start`.
- Go to theme folder and install packages.

```
$ cd content/themes/[theme-name]
$ yarn install
```

- Run `yarn dev` and open http://localhost:2368/.
- Run `yarn zip` and upload zip file(in dist) to theme.