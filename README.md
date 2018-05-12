# Casper SJ 
> Forked from [Hungys](https://github.com/hungys/CasperS)'s [CasperS](https://github.com/hungys/CasperS)

## Intro
A Reivised [Casper theme](https://github.com/TryGhost/Casper) for [My Ghost Blog](https://sujinlee.me/)

### Features

* Vanilla Casper 2.1.1 style
* Works with Ghost 1.2+
* [Google Analytics](http://analytics.google.com) integration
* [Disqus](https://disqus.com) integration
* [Prism](http://prismjs.com)-powered syntax highlight
    * Revised [xonokai.css](https://github.com/PrismJS/prism-themes/blob/master/themes/prism-xonokai.css)
* Social links with [Simple Icons](https://simpleicons.org) integration
* [KaTex](https://khan.github.io/KaTeX/) integration
* Korean Font [Spoaq-han-sans](https://spoqa.github.io/spoqa-han-sans/ko-KR/) intergration

## How to develop your own theme
* Install ghost as following [ghost official docs - install - local](https://docs.ghost.org/docs/install-local)
```
// Install Ghost-CLI
$ yarn global add ghost-cli@latest

// Install Ghost
$ cd /your-ghost-root-directory
$ ghost install local

// Stop Ghost
ghost stop

// install nodemon and gulp globally
$ yarn add -g nodemon@latest
$ yarn add -g gulp
```

* Clone or download the content of repo and put them in `content/themes/` folder under your Ghost installation.
```
$ cd /[your-ghost-root-directory]
$ git clone https://github.com/sujinleeme/CasperSJ.git content/themes/CasperSJ
```

* Install all packages
```
$ yarn add
```

* To complie css/js run gulp.
```
$ cd /[your-ghost-root-directory]/content/themes/casperSJ
$ yarn dev
```

* Start Ghost with nodemon.
```
cd /[your-ghost-root-directory]
$ nodemon current/index.js --watch content/themes/casperSJ --ext hbs,js,css
```

* Open http://localhost:2368/

* Make `.zip` folder into ` dist/<theme-name>.zip`, which you can then upload to your site.
```
$ cd /[your-ghost-root-directory]/content/themes/casperSJ
$ yarn zip
```

# Configuration

You can configure for Google Analytics, Disqus, and social links using Ghost's **Code Injection** feature. Just paste the following example to **Blog Header** section and fill in your information.

```html
<script>
var ga_id = 'UA-xxxxxxxx-x';
var disqus_shortname = 'your-shortname'
var social_link = {
    'linkedin': 'https://www.linkedin.com/in/username',
    'github': 'https://github.com/username',
    'medium': 'https://medium.com/@userid',
    'casper-local': 'https://github.com/hungys/CasperS'
}
</script>
```

For social links, we provide icons for 20 popular services (check the following list). For this kind of services including `'linkedin'` and `'github'`, the icons will be loaded from your website directly. For other services such as `'medium'`, the icons will be loaded from [simpleicons.org](https://simpleicons.org), and you can check the full list on their website and [GitHub](https://github.com/simple-icons/simple-icons/tree/develop/icons). You can also use your custom SVG icons by attaching `-local` suffix to the key, for exmaple, `casper.svg` will be loaded for key `'casper-local'`, and you should prepare the icon and put it under `assets/icons/`.

```
'500px', 'facebook', 'flickr', 'github', 'gmail', 'googleplus', 'instagram', 'line', 'linkedin', 'messenger', 'microsoftoutlook', 'plurk', 'sinaweibo', 'skype', 'snapchat', 'stackoverflow', 'telegram', 'twitter', 'wechat', 'whatsapp'
```

# Copyright & License

Released under the [MIT License](LICENSE).

Copyright (c) 2013-2017 Ghost Foundation (for Casper theme)