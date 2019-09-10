# Customized casper theme(ghost) for developer's personal blog

> Inspired from Hungys's [CasperS](https://github.com/hungys/CasperS)

- [Vanilla Casper 2.11.1 style](https://github.com/TryGhost/Casper)
- Works with Ghost 2+
- Google Analytics integration
- Disqus integration (comments, comment count)
- Prism-powered syntax highlight
- Revised xonokai.css
- Social links with Simple Icons integration
- KaTex

## How to install theme in your live ghost

- Download this repo `zip` file.
- Go to your desgin panel in ghost admin page (https://<ghost-blog-url>/ghost/#/settings/design)
- Click `Upload a theme` button and upload zip file.
- Activate new theme
- Go to code injection panel (https://<ghost-blog-url>/ghost/#/settings/code-injection)
- Update google analytics variable in **Site Header** code block.

```html
<script>
  var ga_id = "your_google_id"
</script>
```

- Update social links and google analytics variables in **Site Footer** code block.
  - Socials icons : facebook, flickr, github, gmail, googleplus', instagram, line, linkedin, messenger, microsoftoutlook, plurk, sinaweibo, skype, snapchat, stackoverflow, telegram, twitter, wechat, whatsapp

```html
<script>
  var social_link = {
    linkedin: "https://www.linkedin.com/in/username",
    github: "https://github.com/username",
    medium: "https://medium.com/@userid"
  }
</script>
```

- Update your disqus shortname in **Site Footer**

```html
<script>
  var disqus_shortname = "sujinlee"
</script>
```

## Katex usage

- Use a pair of single(`$`)/double(`$$`) dollar sign as formula delimiter.

![katex](https://sujinlee.me/content/images/2019/09/katex.png)

## How to customize casper theme

- 한국어 블로그 (Korean)
  - [뚝딱뚝딱 Ghost로 기술 블로그 만들기 - (1) 설치와 호스팅](https://sujinlee.me/how-to-build-ghost-blog/)
  - [뚝딱뚝딱 Ghost로 기술 블로그 만들기 - (2) 블로그 테마 수정하기](https://sujinlee.me/how-to-build-ghost-blog-2/)

* Install ghost locally as following [official setup guide doc](https://ghost.org/docs/install/local/)
* Clone or download the content of repo and put them in `content/themes/` folder under your Ghost installation.

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

- Run `yarn dev` and open localhost.
