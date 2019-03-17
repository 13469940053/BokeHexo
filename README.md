# BlueLake


一个简洁轻量化的响应式[Hexo](https://hexo.io/)博客主题。


[![BlueLake template preview](http://obzf7z93c.bkt.clouddn.com/themeBlueLake.png "BlueLake template preview")](https://chaoo.oschina.io/)

## 安装

### 安装主题和渲染:

```shell
$ git clone https://github.com/chaooo/hexo-theme-BlueLake.git themes/BlueLake
$ npm install hexo-renderer-jade@0.3.0 --save
$ npm install hexo-renderer-stylus --save
```
### 启用

在Hexo配置文件（`hexo/_config.yml`）中把主题设置修改为`BlueLake`。
```  bash
theme: BlueLake
```
如果你想生成压缩后的css，在（`hexo/_config.yml`）中添加：
``` yml
stylus:
  compress: true
```


### 更新

``` bash
cd themes/BlueLake
git pull
```

## 配置
打开`themes/BlueLake/_config.yml`进行配置。

``` yml
##########################
## Site Config Settings ##
##########################

# Theme version
version: 2.0.2

# Theme tone
dark: false #true/false  #切换为true,即可体验深色主题

# Header
menu:
  - page: home
    directory: .
    icon: fa-home
  - page: archive
    directory: archives/
    icon: fa-archive
  - page: about
    directory: about/
    icon: fa-user
  - page: rss
    directory: atom.xml
    icon: fa-rss

# Sidebar
widgets:
  - recent_posts
  - category
  - tag
  - archive
  #- weibo
  - links

# Toc
toc:
  enable: true
  number: false

# Static files
js: js
css: css
share_path: share

# Extensions
Plugins:
  hexo-generator-feed
  hexo-generator-sitemap
  hexo-generator-baidu-sitemap

#Feed Atom
feed:
  type: atom
  path: atom.xml
  limit: 20

#sitemap
sitemap:
  path: sitemap.xml
baidusitemap:
  path: baidusitemap.xml

#Local search
local_search: true ## Use a javascript-based local search engine, true/false.

#Copyright
copyright:
  enable: true #display article copyright information, true/false.
  describe: #copyright description

# MathJax Support
mathjax:
  enable: false  #true/false.
  cdn: //cdn.bootcss.com/mathjax/2.7.1/latest.js?config=TeX-AMS-MML_HTMLorMML

#Cmments
comment:
  duoshuo: #chaooo ## duoshuo_shortname
  disqus: ## disqus_shortname
  livere: ## 来必力(data-uid)
  uyan: ## 友言(uid)
  cloudTie: ## 网易云跟帖(productKey)
  changyan: ## 畅言需在下方配置两个参数，此处不填。
    appid: ## 畅言(appid)
    appkey: ##畅言(appkey)

#Share
local_share: true #本地分享
baidu_share: #true ## 百度分享
JiaThis_share: ##true ##JiaThis分享
duoshuo_share: #true ##true 多说分享必须和多说评论一起使用。

# Analytics
google_analytics: ## Your Google Analytics tracking id, e.g. UA-42025684-2
baidu_analytics: ## Your Baidu Analytics tracking id, e.g. 1006843030519956000

# Miscellaneous
show_category_count: true ## If you want to show the count of categories in the sidebar widget please set the value to true.
widgets_on_small_screens: true ## Set to true to enable widgets on small screens.
busuanzi: true ## If you want to use Busuanzi page views please set the value to true.

# About page
about:
  photo_url: ## Your photo e.g. http://obzf7z93c.bkt.clouddn.com/themeauthor.jpg
  items:
  - label: email
    url: ## Your email with mailto: e.g.  mailto:zhenggchaoo@gmail.com
    title: ## Your email e.g.  zhenggchaoo@gmail.com
  - label: github
    url: ## Your github'url e.g.  https://github.com/chaooo
    title: ## Your github'name e.g.  chaooo
  - label: weibo
    url: ## Your weibo's url e.g.  http://weibo.com/zhengchaooo
    title: ## Your weibo's name e.g.  秋过冬漫长
  - label: twitter
    url:
    title:
  - label: facebook
    url:
    title:

# Friend link
links:
  - title: site-name1
    url: http://www.example1.com/
  - title: site-name2
    url: http://www.example2.com/
  - title: site-name3
    url: http://www.example3.com/
```

- **version** - 用于自动刷新CDN上的静态文件。
- **menu** - 导航菜单。
- **widgets** - 侧边栏中的窗口小部件。
- **Toc** - 文章目录
- **Static files** - 静态文件目录，以方便CDN使用。
- **Local search**
- self_search - 默认本地JS搜索.
- **Cmments**
- duoshuo - 若使用[多说评论](http://duoshuo.com)，注册多说后在这填写short_name(用于评论与分享)。
- disqus - 若使用[Disqus评论](https://disqus.com)，注册Disqus后在这填写short_name。
- livere- 若使用[来必力评论](https://livere.com)，注册来必力,获得data-uid。
- uyan - 若使用[友言评论](http://www.uyan.cc/)，注册友言,获得uid。
- cloudTie - 若使用[网易云跟帖评论](https://gentie.163.com/info.html)，注册网易云跟帖,获得productKey。
- changyan - 若使用[畅言评论](http://changyan.kuaizhan.com)，注册畅言，获得appid，appkey。
- **About page** - 关于我页面(hexo new page 'about')。
- **links** - 友情链接。
- **Miscellaneous**
- show_category_count - 是否在侧边栏分类中显示类别的数量（true/false）.
- widgets_on_small_screens - 小屏幕下侧边栏在底部显示.
- busuanzi - 用[Busuanzi](http://busuanzi.ibruce.info)来统计网站访问量.
- google_analytics - [Google Analytics](https://www.google.com/analytics/) tracking ID。
- baIDu_analytics - [Baidu Analytics](http://tongji.baidu.com) tracking ID。

## 特征

#### 站点图标
您可以准备一张ico格式并命名为** favicon.ico **，请将其放入hexo目录的`source`文件夹，建议大小：32px * 32px。

您可以为苹果设备添加网站徽标，请将名为** apple-touch-icon.png **的图像放入hexo目录的“source”文件夹中，建议大小为：114px * 114px。

#### 添加站点关键字
请在hexo目录的“hexo/_config.yml”中添加`keywords`字段，如：
```YAML
# Site
title: Hexo
subtitle: 副标题
description: 网站简要描述,如：Charles·Zheng's blog.
keywords: 网站关键字, key, key1, key2, key3
author: Charles
language: zh-CN
```

#### 设置阅读全文
您可以在文章的 front-matter 中添加 description，并提供文章摘录，或在文章中使用‘‘`<!--more-->`’’手动进行截断（Hexo推荐的方式）。

#### 自定义page页面
在`source`文件夹中创建文件夹`index.md`来添加页面，并在`index.md`的`front-matter'中添加`layout：page`。
Create folders inlcuding `index.md` in `source` folder to add pages, and add a `layout: page` in `front-matter` of `index.md`.

#### About页面
此主题默认page页面是关于我页面的布局，生成一个关于我页面：
``` shell
$ hexo new page 'about'
```
配置照片地址、邮箱、微博链接、微博名、GitHub链接、Github名：
```YAML
# About page
about:
  photo_url: ## Your photo e.g. http://obzf7z93c.bkt.clouddn.com/themeauthor.jpg
  items:
  - label: email
    icon: fa-email
    url: ## Your email with mailto: e.g.  mailto:zhenggchaoo@gmail.com
    title: ## Your email e.g.  zhenggchaoo@gmail.com
  - label: github
    icon: fa-github
    url: ## Your github'url e.g.  https://github.com/chaooo
    title: ## Your github'name e.g.  chaooo
  - label: weibo
    icon: fa-weibo
    url: ## Your weibo's url e.g.  http://weibo.com/zhengchaooo
    title: ## Your weibo's name e.g.  秋过冬漫长
  - label: twitter
    icon: fa-twitter
    url:
    title:
  - label: facebook
    icon: fa-facebook
    url:
    title:
```
[点击预览About页面](http://chaoo.oschina.io/about/)

#### 代码语法高亮
请在hexo目录的“hexo/_config.yml”中设置“highlight”选项，如下所示：
```YAML
highlight:
  enable: true
  auto_detect: true
  line_number: true
  tab_replace:
```

#### 本地搜索
如果要使用本地站点搜索，您必须安装插件[hexo-generator-json-content](https://github.com/alexbruno/hexo-generator-json-content)来创建JSON搜索文件 ，然后将配置添加到`hexo/_config.yml`：
```shell
$ npm install hexo-generator-json-content@2.2.0 --save
```
然后在`hexo/_config.yml`添加配置：
```YAML
jsonContent:
  meta: false
  pages: false
  posts:
    title: true
    date: true
    path: true
    text: true
    raw: false
    content: false
    slug: false
    updated: false
    comments: false
    link: false
    permalink: false
    excerpt: false
    categories: false
    tags: true
```

#### 语言
该主题目前有七种语言：简体中文（zh-CN），繁体中文（zh-TW），英语（en），法语（fr-FR），德语（de-DE），韩语 （ko）,西班牙语（es-ES）,欢迎修改主题并翻译成其他语言。

## Solutions
- 检查您当前的hexo的根目录，是否包含`source /`，`themes /`等。
- 如果你在使用这个主题有任何问题，请随时打开一个[issue](https://github.com/chaooo/hexo-theme-BlueLake/issues)，或者给我发邮件[zhenggchaoo@gmail.com](zhenggchaoo@gmail.com)。



一、git安装hexo
    1.(新建一个文件夹【电脑的任何位置】)
    2.桌面右键选择 Git Bash
    3.先创建一个文件夹（用来存放所有blog的东西），然后cd到该文件夹下
    3.安装hexo命令npm install hexo-cli -g   【npm i -g hexo】
    4.hexo init #初始化网站
    5.npm install
    6.hexo g #生成或 hexo generate
    7.hexo s #启动本地服务器 或者 hexo server,这一步之后就可以通过http://localhost:4000  查看了

    常用简写
        hexo n == hexo new
        hexo g == hexo generate
        hexo s == hexo server
        hexo d == hexo deploy

二、部署到github上
    1.检查SSH keys的设置
    cd ~/.ssh 检查本机的ssh密钥
    ls

    此时会显示一些文件
        mkdir key_backup
        cp id_rsa* key_backup
        rm id_rsa*
    以上三步为备份和移除原来的SSH key设置

    生成新的 SSH Key：
    ssh-keygen -t rsa -C "2508723631@qq.com" #生成新的key文件,邮箱地址填你的Github地址

    Enter file in which to save the key (/Users/your_user_directory/.ssh/id_rsa):<回车就好>
    然后系统会要你输入密码：
    Enter passphrase (empty for no passphrase):<输入加密串>
    Enter same passphrase again:<再次输入加密串>

    在回车中会提示你输入一个密码，这个密码会在你提交项目时使用，如果为空的话提交项目时则不用输入。这个设置是防止别人往你的项目里提交内容。
    注意：输入密码的时候没有 * 字样的，你直接输入就可以了。


    2.添加SSH Key到Github
        找到 系统当前用户目录下(开启查看隐藏文件) C:\Users\用户名\ .ssh id_rsa.pub文件以文本方式打开。打开之后全部复制到key中

        到了这就可以测试一下是否成功了:

        ssh -T git@github.com
        #之后会要你输入yes/no,输入yes就好了。

        设置你的账号信息:
        git config --global user.name "张成"     #真实名字不是github用户名
        git config --global user.email "2508723631@qq.com"    #github邮箱

    3.部署到github
    hexo d
    但是执行，hexo d报错：

        ERROR Deployer not found: git


    解决方案
        这是因为没安装hexo-deployer-git插件，输入下面的插件安装就好了：

        npm install hexo-deployer-git --save

        然后在使用Hexo -d命令就可以推送了。


    解释一下：
        node_modules：是依赖包
        public：存放的是生成的页面
        scaffolds：命令生成文章等的模板
        source：用命令创建的各种文章
        themes：主题
        _config.yml：整个博客的配置
        db.json：source解析所得到的
        package.json：项目所需模块项目的配置信息
    做好这些前置工作之后接下来的就是各种配配配置了。



三、这里介绍一下怎么创建一篇文章
    hexo new "文章名" #新建文章
    hexo new page "页面名" #新建页面

    新建一篇文章后就可以预览了,在hexo new之后执行一次生成hexo g再执行hexo s启动本地服务器,如果之前还在hexo s 按Ctrl + C 结束.

四、添加主题
    安装主题(yilia主题):
        hexo clean
        git clone https://github.com/litten/hexo-theme-yilia.git themes/yilia
    启动主题
        找到目录下的_config.yml 文件,打开找到 theme：属性并设置为yilia

    更新主题
        cd themes/yilia
        git pull
        hexo g
        hexo s
    此时刷新http://localhost:4000/页面就能看到新的主题了.

    使用Hexo deploy部署到github
    还是编辑根目录下_config.yml文件

    deploy:
        type: git
        repo: git@github.com:cczeng/cczeng.github.io.git  #这里的网址填你自己的
        branch: master


    具体配置可参考我的博客备份

    保存后需要提前安装一个扩展：

    npm install hexo-deployer-git --save
    接下来就是将Hexo部署到我们的Github仓库上

landscape
安装BlueLake主题和渲染:
    $ git clone https://github.com/chaooo/hexo-theme-BlueLake.git themes/BlueLake
    $ npm install hexo-renderer-jade@0.3.0 --save
    $ npm install hexo-renderer-stylus --save
    启用
    在Hexo配置文件（hexo/_config.yml）中把主题设置修改为BlueLake。

    theme: BlueLake
    如果你想生成压缩后的css，在（hexo/_config.yml）中添加：

    stylus:
      compress: true
    更新
    cd themes/BlueLake
    git pull



