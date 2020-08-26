---
title: Hexo二次元主题之Sakura
author: ちい
avatar: https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/custom/avatar.jpg
authorLink: www.basaka.ga  #作者的域名
authorAbout:  #关于
authorDesc:   #作者描述
categories: 技术
date: 
comments: true  # 是否需要留言
tags:      # 下面可以写多个标签
   - Hexo
   - Sakura主题
keywords: Hexo博客部署  # 文章关键词
description:    #文章描述
photos: https://cdn.jsdelivr.net/gh/liufg520/Blog-Pictures/%E8%83%8C%E6%99%AF%E5%9B%BE/20200818222114.png
---

# 前言：（未完成）

**如何选择一款适合自己的主题呢？如果你是极简主义者：推荐Next主题，如果你和我一样喜欢二次元主题，强烈推荐Sakura主题。如果担心自己看不懂源代码又特别喜欢这个主题该怎么办呢？为此特意整理记录了此篇教程。切记切记不要无脑复制，有些配置已经配置过，无需重复配置。请多多使用F12开发者工具去校对修改，博客页面中涉及到图标、字符等等资源的样式都可以用开发者工具去调试修改。对于问题的排错，也是很方便的利器呢。接下来就使用魔法让博客变得更漂亮吧！**

# 一.主题资源下载安装

**1.首先下载Sakura主题与资源这2个部分，下载地址：**

**① Sakura主题下载地址：https://pan.baidu.com/s/1QIfVtWPAqDSHijc63rBfHQ 提取码:dr9w**

**② Sakura资源下载地址：https://pan.baidu.com/s/1ZogVBWiuSlqsp8imfNXlRg 提取码:4155**

**2.解压安装Sakura主题：使用解压软件解压Hexo-Sakura主题.rar，将Hexo-Sakura文件夹里的文件上传到博客的根目录，重复的文件选择替换。可使用Xftp上传文件到博客根目录。🔖注释：根目录指的就是你安装初始化Hexo的那个目录**

![](https://cdn.jsdelivr.net/gh/liufg520/Blog-Pictures/%E7%BD%91%E7%BB%9C/Hexo-Sakura%E4%B8%BB%E9%A2%98%E7%9B%AE%E5%BD%95%E7%BB%93%E6%9E%84.gif)

**3.解压修改Sakura资源：使用解压软件解压SakuraCDN.rar，SakuraCDN文件夹里主要包含404页面、图片，字体，脚本等资源文件。根据《主题资源美化修改》将需要替换资源文件替换成自己的文件。🔖注释：建议使用Vscode或者webstorm编辑器修改**

![](https://cdn.jsdelivr.net/gh/liufg520/Blog-Pictures/%E7%BD%91%E7%BB%9C/Hexo-SakuraCDN%E8%B5%84%E6%BA%90%E7%9B%AE%E5%BD%95%E7%BB%93%E6%9E%84.gif)

**4.搭建Sakura主题资源CDN：登陆自己的Github新建仓库作为Sakura主题资源的CDN存储，根据《主题资源美化修改》将整理修改好的资源文件上传到GitHub仓库即可。🔖注释：为了方便省事儿建议以下凡是涉及到调用CDN资源的请使用原有的文件名并保持文件路径不变，这样你只需要将原有的CDN地址前缀替换成你的CDN地址前缀就可以了。CDN地址前缀一般为[https://cdn.jsdelivr.net/gh/你的GitHub账号/你的CDN仓库名/](https://cdn.jsdelivr.net/gh/你的GitHub账号/你的CDN仓库名/)⇨具体如何搭建CDN请参考《使用Github+jsdelivr搭建属于自己的CDN》**

**5.安装依赖：在命令行输入`npm i`**

# 二.文件目录结构分析                                                                    

**📌Sakura主题文件目录分析：**

![](https://cdn.jsdelivr.net/gh/liufg520/Blog-Pictures/%E7%BD%91%E7%BB%9C/Hexo-Sakura%E4%B8%BB%E9%A2%98%E6%96%87%E4%BB%B6%E7%9B%AE%E5%BD%95%E5%88%86%E6%9E%90%E5%9B%BE.gif)

​                                                                                          





# 三.涉及到的工具分类

**1.在线创意二维码制作网址：http://www.qmacode.com ⇨描述：制作美化属于自己的个性二维码**

**2.在线Favicon图标制作网址：https://tool.lu/favicon ⇨描述：制作网站图标，可在线将图片转换成ico格式**

**3.在线文件格式转换网址：https://cloudconvert.com ⇨描述：转换图片格式，字体格式，制作鼠标指针等等**

**4.在线自定义鼠标光标：https://custom-cursor.com/en/constructor ⇨描述：下载光标图片转换成cur格式即可**



# 四.主题资源美化修改

## 1.博客目录的_config配置

**📜文件位置：Hexo根目录/_config.yml**

  **📄修改内容：网站标题、简介、署名**

  **📃修改配置：空白项可不填**

```
# Site
title: 🌈ちいの小本🎈 
subtitle:
description: 介里是萌萌的二次元喵~ 
keywords: 
author: ちい 
language: zh-cn
timezone:
```

## 2.主题目录的_config配置

**📜文件位置：Hexo根目录/themes/Sakura/_config.yml**

  **📄修改内容：网站名称**

  **📃修改配置：prefixName为站点名字前缀，siteName是你站点名字。**

```
# site name 
prefixName: さくら村の
siteName: 小叽
```

  **📄修改内容： 网站Favicon图标、avatar头像、描述、URL、CDN、首页notice通告、懒加载lazyloadImg**

  **📃修改配置：找到对应CDN资源文件，例如找到img/custom/avatar.jpg文件将avatar.jpg文件替换成自己的头像，文件名不变。**

```
# favicon and site master avatar
favicon: /img/custom/Favicon.ico 
avatar: /img/custom/avatar.jpg
url: https://liqian.5201314920.xyz 
description: 只要有想见的人，就不再是孤身一人了。
cdn: https://cdn.jsdelivr.net/gh/你的GitHub账号/你的CDN仓库名
pjax: 1
notice: (。•﹃ •。)即使我弱了，也不代表你强了
lazyloadImg: https://cdn.jsdelivr.net/gh/GitHub账号/CDN仓库名/img/loader/orange.progress-bar-stripe-loader.svg 
```

   **📄修改内容： 网站导航菜单栏配置，根据自己的需要修改**

   **📃修改配置：修改菜单名，不需要的菜单栏可以删掉。注意菜单栏格式，二级菜单最后末尾是没有逗号的。菜单栏图标修改举例⇨fa: fa-book是菜单图标名可修改。菜单栏图标地址：http://www.fontawesome.com.cn/faicons**

```
menus:
  首页: { path: /, fa: fa-toggle-on faa-shake }
  归档: { path: /archives, fa: fa-archive faa-shake, submenus: { 
    技术: {path: /categories/技术/, fa: fa-globe }, 
    娱乐: {path: /categories/娱乐/, fa: fa-bomb }, 
    灵感: {path: /categories/灵感/, fa: fa-eercast},
    笔记: {path: /categories/笔记/, fa: fa-book }
  } }
  清单: { path: javascript:;, fa: fa-list-ul faa-vertical, submenus: { 
    日语: {path: /tags/日语/, fa: fa-language faa-bounce }, 
    番组: {path: /bangumi/, fa: fa-youtube-play faa-vertical }, 
    歌单: {path: /music/, fa: fa-headphones },
    绘画: {path: /tags/绘画/, fa: fa-paint-brush }
  } }
  标签: {path: /tags/, fa: fa-tag }
  分类: {path: /categories/, fa: fa-bookmark }
  留言: { path: /comment/, fa: fa-paper-plane-o }
  友链: { path: /links/, fa: fa-link faa-shake }
  赞赏: { path: /donate/, fa: fa-heart faa-pulse }
  关于: { path: /, fa: fa-leaf faa-wrench , submenus: { 
    我？: {path: /about/, fa: fa-meetup}, 
     RSS: { path: /atom.xml, fa: fa-rss faa-pulse }
  } }
```

  **📄修改内容： 首页背景图、背景样式、首页startdash相关配置**

  **📃修改配置：首页背景图替换，建议将图片格式转换成webp格式。4种背景图样式根据自己的喜好修改。修改startdash对应参数。**

```
# 首页背景图片 
bg:
  - https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cover/bg1.webp
  - https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cover/bg2.webp
  - https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cover/bg3.webp
  - https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cover/bg4.webp
  - https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cover/bg5.webp
  - https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cover/bg6.jpg
# 背景图片样式 空 原图效果 filter-dim 阴影 filter-grid 横条 filter-dot 点点
bgclass: filter-grid
# startdash url, title, desc img 
startdash: 
  - {url: https://www.ted.com/talks?sort=newest&language=zh-tw, title: 技术、娱乐、设计, desc: 值得传播的视频, img: /img/startdash/QQkongjian.jpg}
  - {url: http://lackk.com, title: 兰客创意, desc: 分享创意及美的一切, img: /img/startdash/QQyinyue.jpg}
  - {url: https://zh.wikihow.com, title: 万事指南, desc: 汇聚各个领域值得信赖的研究与专业知识, img: /img/startdash/DMweimei.jpg}
# your site build time or founded date
#
siteBuildingTime: 07/07/2020
```

  **📄修改内容： 电脑端⇨社交配置 **

  **📃修改配置：url改为自己的链接，img可以不改，不需要的社交配置可删除。**

```
#social  url, img PC端配置
social:
  github: {url: http://github.com/liufg520, img: /img/social/github.png}
  sina: {url: http://weibo.com/liufg520?is_all=1, img: /img/social/sina.png}
  wangyiyun: {url: http://music.163.com/playlist?id=2149082231, img: /img/social/wangyiyun.png}
  zhihu: {url: https://www.zhihu.com/people/a-liang-85-58, img: /img/social/zhihu.png}
  email: {url: http://mail.qq.com/cgi-bin/qm_share?t=qm_mailme&email=945356012@qq.com, img: /img/social/email.svg}
  wechat: {url: /#, qrcode: /img/custom/wechat.jpg, img: /img/social/wechat.png}
```

  **📄修改内容： 手机端⇨社交配置 **

  **📃修改配置：url改为自己的链接，img可以不改，不需要的社交配置可删除。**

```
#social  url, img 移动端配置
msocial:
  github: {url: http://github.com/liufg520, fa: fa-github, color: 333}
  weibo: {url: http://weibo.com/liufg520?is_all=1, fa: fa-weibo, color: dd4b39}
  qq: {url: mqqwpa://im/chat?chat_type=wpa&uin=945356012&version=1&src_type=web&web_src=lvlingseeds.com, fa: fa-qq, color: 25c6fe}
```

  **📄修改内容： 赞赏二维码 **

  **📃修改配置：替换url和二维码图片。**

```
# 赞赏二维码 #
donate:
  paypal: https://www.paypal.me/liufg
  alipay: /img/custom/donate/AlipayQR.jpg
  wechat: /img/custom/donate/wechanQR.jpg
  wechatSQ: /img/custom/donate/WeChanSQ.jpg
```

  **📄修改内容： 首页媒体视频、左下角悬浮歌单 **

  **📃修改配置：替换视频文件，替换网易音乐id值⇨使用浏览器登陆网易云音乐打开我的音乐可以在浏览器地址栏看到对应id数值。**

```
# 视频地址为https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/BeautifulWorld.mp4，配置如下
movies:
  url: https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN
  # 多个视频用逗号隔开，随机获取。支持的格式目前已知MP4,Flv。其他的可以试下，不保证有用
  name: BeautifulWorld.mp4
 #音乐播放器    
aplayer: 
  id: 2149082231
  server: netease
  type: playlist
  fixed: true
  autoplay: false
  loop: all
  order: random
  preload: auto
  volume: 0.7
  mutex: true
```

  **📄修改内容： Valine评论系统**

  **📃修改配置：需要注册leancloud账号：https://www.leancloud.cn然后获取id和key 。可参考官网文档：https://valine.js.org**

```
# Valine ##极简留言功能
# You can get your appid and appkey from https://leancloud.cn
# more info please open https://valine.js.org
valine:
  enable: true ##打开valine评论功能true
  appId: 填你自己leancloud获取的ID
  appKey: 填你自己leancloud获取的key
  notify: false #评论mail回复提醒
  verify: false #验证码
  visitor: false #统计阅读量
  avatar: wavatar #自定义头像
  guest_info: nick,mail,link #评论者相关信息 
  pageSize: 10 #评论列表分页，每页条数
  lang: zh-cn # 自定义语言
  palaceholder: 昵称填写qq可以显示qq头像和昵称哦~ 
  recordIP: true # 是否记录评论者IP
  serverURLs: '' 
  count: true # top_img显示评论数
```

## 3.分类页和标签页配置

**📜文件位置：Hexo根目录/themes/Sakura/languages/zh-cn.yml**

  **📄修改内容：分类页和标签页**

  **📃修改配置：如果新增一个分类或者标签在这里添加相关配置。如何新增分类页和标签页请参考Hexo官网文档**

```
#category 分类页，其它分类按照这个格式创建
技术:
    zh: 网络安全 #中文标题
    en: Network Security # 英文标题
    img: https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/banner/Coding.webp  # 封面图片
#tag  标签页，标签名即是标题
灵感:                              
    img: https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/banner/inspiration.webp  # 封面图片
```

## 4.添加优美的标签页

**📋创建文件：layout/tags.ejs、_widget/tag-cloud.ejs，tag-wordcloud.ejs**

**① 在tags.ejs添加以下代码**

```
<%- partial('_partial/header') %>
<main class="content">
    <%- partial('_widget/tag-cloud') %>
    <%- partial('_widget/tag-wordcloud') %>
</main>
```

**② 在tag-cloud.ejs添加以下代码**

```
<%
var colorArr = ['#F9EBEA', '#F5EEF8', '#D5F5E3', '#E8F8F5', '#FEF9E7',
    '#F8F9F9', '#82E0AA', '#D7BDE2', '#A3E4D7', '#85C1E9', '#F8C471', '#F9E79F', '#FFF'];
var colorCount = colorArr.length;
var hashCode = function (str) {
    if (!str && str.length === 0) {
        return 0;
    }
    var hash = 0;
    for (var i = 0, len = str.length; i < len; i++) {
        hash = ((hash << 5) - hash) + str.charCodeAt(i);
        hash |= 0;
    }
    return hash;
};
var i = 0;
var isTag = is_tag();
%>
<div id="tags" class="container chip-container">
    <div class="card">
        <div class="card-content">
            <div class="tag-title center-align">
                <i class="fa fa-tags"></i>&nbsp;&nbsp;文章标签
            </div>
            <div class="tag-chips">
                <% site.tags.map(function(tag) { %>
                <%
                    i++;
                    var color = i >= colorCount ? colorArr[Math.abs(hashCode(tag.name) % colorCount)]
                            : colorArr[i - 1];
                %>
                <a href="<%- url_for(tag.path) %>" title="<%- tag.name %>: <%- tag.length %>">
                    <span class="chip center-align waves-effect waves-light
                            <% if (isTag && tag.name == page.tag) { %> chip-active <% } else { %> chip-default <% } %>"
                            data-tagname="<%- tag.name %>" style="background-color: <%- color %>;"><%- tag.name %>
                        <span class="tag-length"><%- tag.length %></span>
                    </span>
                </a>
                <% }); %>
            </div>
        </div>
    </div>
</div>
```

**③ 在tag-wordcloud.ejs添加以下代码**

```
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/gh/wallleap/cdn/css/jqcloud.css">
<style type="text/css">
    #tag-wordcloud {
        width: 100%;
        height: 300px;
    }
</style>
<div class="container" data-aos="fade-up">
    <div class="card">
        <div id="tag-wordcloud" class="card-content"></div>
    </div>
</div>
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.4.4/jquery.min.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/wallleap/cdn/js/jqcloud-1.0.4.js"></script>
<script type="text/javascript">
    <%
    let tagWordArr = [];
    site.tags.map(function(tag) {
        tagWordArr.push({'text': tag.name, 'weight': tag.length, 'link': tag.permalink});
    });
    let tagWords = JSON.stringify(tagWordArr);
    %>
    $('#tag-wordcloud').jQCloud(<%- tagWords %>, {
        autoResize: true
    });
</script>
```

**④ 在style.css末尾添加以下代码**

```
.chip-container {    margin-top: 60px;}.chip-container .tag-title {    margin-bottom: 10px;    color: #3C4858;    font-size: 1.75rem;    font-weight: 400;}.chip-container .tag-chips {    margin: 1rem auto 0.5rem;    max-width: 850px;    text-align: center;}.chip-container .tags-posts {    margin-top: 20px;}.chip-container .chip-default {    color: #34495e;}.chip-container .chip-active {    color: #FFF !important;    background: linear-gradient(to bottom right, #FF5E3A 0%, #FF2A68 100%) !important;    box-shadow: 2px 5px 10px #aaa !important;}.chip-container .chip {    margin: 10px 10px;    padding: 19px 14px;    display: inline-flex;    line-height: 0;    font-size: 1rem;    font-weight: 500;    border-radius: 5px;    cursor: pointer;    box-shadow: 0 3px 5px rgba(0, 0, 0, .12);}.chip-container .chip:hover {    color: #fff;    background: linear-gradient(to right, #4cbf30 0%, #0f9d58 100%) !important;}.chip .tag-length {    margin-left: 5px;    margin-right: -2px;    font-size: 0.5rem;}.chip-default .tag-length {    color: #e91e63;    margin-top: 1px;}.chip-active .tag-length {    color: #fff;}.tag-title.center-align{    margin-top: 100px;    text-align : center;}
```

**⑤ 使用命令`hexo new page "tags"`，修改博客根目录下source/tags/index.md**

```
---
title: tags
date: 2020-07-18 13:50:05
layout: tags
---
```

## 5.添加优美的分类页

**📋创建文件：layout/categories.ejs、_widget/category-cloud.ejs，category-radar.ejs**

**📄添加代码：**

**① 在categories.ejs添加以下代码**

```
<%- partial('_partial/header') %>
<main class="content">
    <%- partial('_widget/category-cloud') %>
    <% if (site.categories && site.categories.length > 0) { %>
    <%- partial('_widget/category-radar') %>
    <% } %>
</main>
```

**② 在category-cloud.ejs添加以下代码**

```
<%
var colorArr = ['#F9EBEA', '#F5EEF8', '#D5F5E3', '#E8F8F5', '#FEF9E7',
    '#F8F9F9', '#82E0AA', '#D7BDE2', '#A3E4D7', '#85C1E9', '#F8C471', '#F9E79F', '#FFF'];
var colorCount = colorArr.length;
var hashCode = function (str) {
    if (!str && str.length === 0) {
        return 0;
    }
    var hash = 0;
    for (var i = 0, len = str.length; i < len; i++) {
        hash = ((hash << 5) - hash) + str.charCodeAt(i);
        hash |= 0;
    }
    return hash;
};
var i = 0;
var isCategory = is_category();
%>
<div id="category-cloud" class="container chip-container">
    <div class="card">
        <div class="card-content">
            <div class="tag-title center-align">
                <i class="fa fa-bookmark"></i>&nbsp;&nbsp;文章分类
            </div>
            <div class="tag-chips">
                <% if (site.categories && site.categories.length > 0) { %>
                <% site.categories.map(function(category) { %>
                <%
                    i++;
                    var color = i >= colorCount ? colorArr[Math.abs(hashCode(category.name) % colorCount)]
                            : colorArr[i - 1];
                %>
                <a href="<%- url_for(category.path) %>" title="<%- category.name %>: <%- category.length %>">
                    <span class="chip center-align waves-effect waves-light
                            <% if (isCategory && category.name == page.category) { %> chip-active <% } else { %> chip-default <% } %>"
                            style="background-color: <%- color %>;"><%- category.name %>
                        <span class="tag-length"><%- category.length %></span>
                    </span>
                </a>
                <% }); %>
                <% } else { %>
                <%= __('categoryEmptyTip') %>
                <% } %>
            </div>
        </div>
    </div>
</div>
```

**③ 在category-radar.ejs添加以下代码**

```
<style type="text/css">
    #category-radar {
        margin-top: 50px;
        width: 100%;
        height: 360px;
    }
</style>
<div class="container" data-aos="fade-up">
    <div class="card">
        <div id="category-radar" class="card-content"></div>
    </div>
</div>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/wallleap/cdn/js/echarts.min.js"></script>
<script type="text/javascript">
    let radarChart = echarts.init(document.getElementById('category-radar'));
    <%
        var categories = site.categories;
        // Find the maximum and average values of the post categories.
        var radarValueArr = [];
        categories.some(function(category) {
            radarValueArr.push(category.length);
        });
        var max = Math.max.apply(null, radarValueArr) + Math.min.apply(null, radarValueArr);
        // Calculate the data needed for the radar chart.
        var indicatorArr = [];
        categories.map(function(category) {
            indicatorArr.push({'name': category.name, 'max': max});
        });
        var indicatorData = JSON.stringify(indicatorArr);
        var radarValueData = JSON.stringify(radarValueArr);
    %>
    let option = {
        title: {
            left: 'center',
            text: '文章分类雷达图',
            textStyle: {
                fontWeight: 500,
                fontSize: 22
            }
        },
        tooltip: {},
        radar: {
            name: {
                textStyle: {
                    color: '#3C4858'
                }
            },
            indicator: <%- indicatorData %>,
            nameGap: 5,
            center: ['50%','55%'],
            radius: '66%'
        },
        series: [{
            type: 'radar',
            color: ['#3ecf8e'],
            itemStyle: {normal: {areaStyle: {type: 'default'}}},
            data : [
                {
                    value : <%- radarValueData %>,
                    name : '文章分类数量'
                }
            ]
        }]
    };
    radarChart.setOption(option);
</script>
```

**④ 使用命令`hexo new page "categories"`，修改博客根目录下source/categories/index.md**

```
---
title: categories
date: 2020-03-09 13:50:05
layout: categories
---
```

**⑤ 修改主题配置文件⇨Hexo根目录/themes/Sakura/_config.yml，将这两行代码放到留言之前**

```
  标签: {path: /tags/, fa: fa-tag }
  分类: {path: /categories/, fa: fa-bookmark }
```

## 6.单页面封面配置

**📂每个单页面文件夹存放位置：Hexo根目录/source/**

**📜每个单页面文件位置：例如留言板页面⇨Hexo根目录/source/comment/index.md**

  **📄修改内容：单页面封面图片**

  **📃修改配置：photos: ⇨换成你喜欢的封面图片哦~**

```
title: comment
date: 2020-07-02 23:13:48
keywords: 
description: 
comments: true
photos: https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/banner/Comment.webp 
```

## 7.番组单页面配置

**📜番组单页面文件位置：Hexo根目录/source/bangumi/index.md**

  **📄修改内容：番组计划页面**

  **📃修改配置：按照bangumis参数格式修改添加番组计划表哦~**

```
layout: bangumi
title: bangumi
comments: false
date: 2020-08-17 21:32:48
keywords:
description:
bangumis:
  - img: https://lain.bgm.tv/pic/cover/l/0e/1e/218971_2y351.jpg
    title: 朝花夕誓——于离别之朝束起约定之花
    status: 已追完
    progress: 100
    jp: さよならの朝に約束の花をかざろう
    time: 2018-02-24 SUN.
    desc: 住在远离尘嚣的土地，一边将每天的事情编织成名为希比欧的布，一边静静生活的伊欧夫人民。在15岁左右外表就停止成长，拥有数百年寿命的他们，被称为“离别的一族”，并被视为活着的传说。没有双亲的伊欧夫少女玛奇亚，过着被伙伴包围的平稳日子，却总感觉“孤身一人”。他们的这种日常，一瞬间就崩溃消失。追求伊欧夫的长寿之血，梅萨蒂军乘坐着名为雷纳特的古代兽发动了进攻。在绝望与混乱之中，伊欧夫的第一美女蕾莉亚被梅萨蒂带走，而玛奇亚暗恋的少年克里姆也失踪了。玛奇亚虽然总算逃脱了，却失去了伙伴和归去之地……。
```

## 8.友链单页面配置

**📜友链单页面文件位置：Hexo根目录/source/links/index.md**

  **📄修改内容：添加友链**

  **📃修改配置：按照links参数格式修改添加友链哦~**

```
layout: links
title: links
date: 2018-12-19 23:11:06
keywords: 友人帐
description: 
comments: true
photos: https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/banner/Links.webp
links:
  - group: 个人项目
    desc: 充分说明这家伙是条咸鱼 < (￣︶￣)>
    items:
    - url: https://shino.cc/fgvf
      img: https://cloud.moezx.cc/Picture/svg/landscape/fields.svg
      name: Google
      desc: Google 镜像
```

## 9.关于单页面配置

**📜文件位置：js/botui.js**

  **📄修改内容：关于⇨我？对话内容修改**

  **📃修改配置：主要修改content后面双引号里的内容**

![](https://cdn.jsdelivr.net/gh/liufg520/Blog-Pictures/%E7%BD%91%E7%BB%9C/%E5%85%B3%E4%BA%8E%E2%80%94%E6%88%91%EF%BC%9F%E5%AF%B9%E8%AF%9D%E5%86%85%E5%AE%B9%E4%BF%AE%E6%94%B9.gif)

## 10.页面预加载配置

**📜文件位置：themes/Sakura/layout/layout.ejs**

  **📄代码功能：使网站页面在1 分钟内即时。官网：https://instant.page**

  **📃添加代码：在layout.ejs首行添加以下代码。**

```
<!-- 页面预加载 --><script src="//instant.page/5.1.0" type="module" integrity="sha384-by67kQnR+pyfy8yWP4kPO12fHKRLHZPfEsiSXR8u2IKcTdxD805MGUXBzVPnkLHw"></script>
```

## 11.添加不蒜子计数

**📜文件位置：themes/Sakura/layout/layout.ejs**

  **📄代码功能：查看访问量pv、用户访问量uv使用**

  **📃添加代码：在layout.ejs末尾添加以下代码。**

```
<!--不蒜子计数器 --><script src="//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js"></script>
```

## 12.添加美化特效

**📜文件位置：themes/Sakura/layout/layout.ejs**

  **📄添加特效：鼠标点击、移动特效**

  **📃添加代码：在layout.ejs末尾添加以下代码，点击特效可组合。**

```
<!-- 点击出现爱心 --><script src="https://cdn.jsdelivr.net/gh/wallleap/cdn/js/love.js"></script>
<!-- 鼠标移动特效彩色雪花 --><script src="https://cdn.jsdelivr.net/gh/wallleap/cdn/js/xuehua.js"></script>
<!-- 点击出现社会主义文字 --><script src="https://cdn.jsdelivr.net/gh/wallleap/cdn/js/shehuizhuyi.js"></script>
<!-- 点击出现彩色气球爆炸效果 --><canvas class="fireworks" style="position: fixed;left: 0;top: 0;z-index: 1; pointer-events: none;" ></canvas> <script type="text/javascript" src="//cdn.bootcss.com/animejs/2.2.0/anime.min.js"></script> 
<script src="https://cdn.jsdelivr.net/gh/wallleap/cdn/js/clickBom.js"></script>
```

**🎁彩色气球爆炸特效展示，其它特效自行测试：**

![](https://cdn.jsdelivr.net/gh/liufg520/Blog-Pictures/%E7%BD%91%E7%BB%9C/%E9%BC%A0%E6%A0%87%E7%82%B9%E5%87%BB%E6%B0%94%E7%90%83%E7%88%86%E7%82%B8%E7%89%B9%E6%95%88%E5%B1%95%E7%A4%BA.gif)

  **📄添加特效：背景特效⇨①飘动彩带 ②动态线条（任意选一个即可）**

  **📃添加代码：在layout.ejs末尾添加以下代码。**

```
<!-- 飘动彩带 --><script src="https://cdn.jsdelivr.net/gh/wallleap/cdn/js/piao.js"></script>
<!-- 动态线条 --><script src="https://cdn.jsdelivr.net/gh/wallleap/cdn/js/canvas-nest.min.js"></script>
```

**🎁彩色飘带背景特效展示：**

![](https://cdn.jsdelivr.net/gh/liufg520/Blog-Pictures/%E7%BD%91%E7%BB%9C/%E5%BD%A9%E8%89%B2%E9%A3%98%E5%B8%A6%E8%83%8C%E6%99%AF%E7%89%B9%E6%95%88.gif)

**🎁动态线条背景特效展示：**

![](https://cdn.jsdelivr.net/gh/liufg520/Blog-Pictures/%E7%BD%91%E7%BB%9C/%E5%8A%A8%E6%80%81%E7%BA%BF%E6%9D%A1%E8%83%8C%E6%99%AF%E7%89%B9%E6%95%88.gif)

**📄添加特效：漂浮物特效⇨①樱花飘落 ②雪花飘落（任意选一个即可）**

**📃添加代码：在layout.ejs末尾添加以下代码。**

```
<!-- 樱花飘落特效 --><script src="https://cdn.jsdelivr.net/gh/wallleap/cdn/js/sakura.js"></script>
<!-- 雪花飘落特效 --><script src="https://cdn.jsdelivr.net/gh/wallleap/cdn/js/xuehuapiaoluo.js"></script>
```

**🎁樱花飘落特效展示：**

![](https://cdn.jsdelivr.net/gh/liufg520/Blog-Pictures/%E7%BD%91%E7%BB%9C/%E6%A8%B1%E8%8A%B1%E9%A3%98%E8%90%BD%E6%BC%82%E6%B5%AE%E7%89%A9%E7%89%B9%E6%95%88%E5%B1%95%E7%A4%BA.gif)

**🎁雪花飘落特效展示：**

![](https://cdn.jsdelivr.net/gh/liufg520/Blog-Pictures/%E7%BD%91%E7%BB%9C/%E9%9B%AA%E8%8A%B1%E9%A3%98%E8%90%BD%E6%BC%82%E6%B5%AE%E7%89%A9%E7%89%B9%E6%95%88%E5%B1%95%E7%A4%BA.gif)

**📄添加Live2D看板娘：可更换人物模型和皮肤哦~**

**📃添加代码：在layout.ejs末尾添加以下代码。**

```
<!--看板娘--><script src="https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/Live2d/autoload.js"></script> 
```

**💖如何设置看板娘默认皮肤❓**

**① 打开浏览器开发者工具，在控制台查看Live2D模型参数值**

**② 修改Liv2d目录下的waifu-tips.js文件，填入对应模型材质ID即可**

![](https://cdn.jsdelivr.net/gh/liufg520/Blog-Pictures/%E7%BD%91%E7%BB%9C/%E5%A6%82%E4%BD%95%E8%AE%BE%E7%BD%AE%E7%9C%8B%E6%9D%BF%E5%A8%98%E9%BB%98%E8%AE%A4%E7%9A%AE%E8%82%A4.gif)

## 13.禁用一些按键

**📜文件位置：themes/Sakura/layout/layout.ejs**

  **📄代码功能：禁用了鼠标右键，还可以开启禁用鼠标左键拖动选择文字**

  **📃添加代码：在layout.ejs末尾添加以下代码。**

```
<!-- 禁用按键 --><script src="https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/js/noSomeKey.js"></script>
```

## 14.添加一言语句

**📜文件位置：themes/Sakura/layout/headertop.ejs**

  **📄修改内容：将社交配置图标上方描述替换成一言语句**

  **📃修改配置：将描述语句注释掉，添加替换成一言API。具体可参考一言官网：https://developer.hitokoto.cn**

```
<!-- 找到这个位置 --><div class="header-info">  
<!-- 把这句注释掉 <p><%= theme.description %></p> --> 
<!-- 添加一言语句 -->
<p id="hitokoto">:D 获取中...</a></p>
<script src="https://v1.hitokoto.cn/?c=a&max_length=24&encode=js&select=%23hitokoto" defer></script>
```

## 15.添加网站运行时间

**📜文件位置：themes/Sakura/layout/footer.ejs**

  **📄修改内容：添加网站运行时间**

  **📃修改配置：载入天数和载入时分秒这2句代码放在适合的位置即可**

```
<!-- 在博客底部添加网站运行时间 -->
<span id="timeDate">载入天数...</span>
<span id="times">载入时分秒...</span>
<script>
  var now = new Date();
  function createtime() {
    var grt= new Date("07/07/2020 16:44:00");//此处修改你的建站时间或者网站上线时间
    now.setTime(now.getTime()+250);
    days = (now - grt ) / 1000 / 60 / 60 / 24; dnum = Math.floor(days);
    hours = (now - grt ) / 1000 / 60 / 60 - (24 * dnum); hnum = Math.floor(hours);
    if(String(hnum).length ==1 ){hnum = "0" + hnum;} minutes = (now - grt ) / 1000 /60 - (24 * 60 * dnum) - (60 * hnum);
    mnum = Math.floor(minutes); if(String(mnum).length ==1 ){mnum = "0" + mnum;}
    seconds = (now - grt ) / 1000 - (24 * 60 * 60 * dnum) - (60 * 60 * hnum) - (60 * mnum);
    snum = Math.round(seconds); if(String(snum).length ==1 ){snum = "0" + snum;}
    document.getElementById("timeDate").innerHTML = "本站已运行 "+dnum+" 天 ";
    document.getElementById("times").innerHTML = hnum + " 小时 " + mnum + " 分 " + snum + " 秒";
  }
  setInterval("createtime()",250);
</script>
```

## 16.添加主题切换工具

**📜文件位置：themes/Sakura/layout/footer.ejs**

  **📄修改内容：添加右下角主题切换工具栏**

  **📃添加代码：不需要的工具按钮可选择注释**

```
<!--网站底部主题切换工具栏-->
    <div class="skin-menu no-select" id="mainskin" style="position: fixed">
      <div class="theme-controls row-container">
       <ul class="menu-list">
        <li id="white-bg"> <i class="iconfont icon-sakura"></i></li>
        <li id="dark-bg"> <i class="iconfont icon-time"></i></li>
        <li id="KAdots-bg"> <i class="iconfont icon-dots"></i></li>
        <li id="pixiv-bg"> <i class="iconfont icon-pixiv"></i></li>
        <!--<li id="sakura-bg"> <i class="iconfont icon-sakura"></i></li>
        <li id="gribs-bg"> <i class="iconfont icon-notice"></i></li>
        <li id="totem-bg"> <i class="iconfont icon-message"></i></li>
        <li id="bing-bg"> <i class="iconfont icon-bing"></i></li>-->
       </ul>
      </div>
     </div>
     <canvas id="night-mode-cover"></canvas>
     <div class="changeSkin-gear no-select cc_pointer" style="visibility: visible; bottom: 0px;">
      <div class="keys cc_pointer" id="setbtn"> 
       <span id="open-skinMenu"> 阅读模式 | SCHEME TOOL  
         <i class="iconfont icon-gear inline-block rotating cc_pointer"></i> 
       </span>
      </div>
    </div>
```

## 17.修改鼠标指针样式

**📜代码文件位置：css/style.css**

**📜资源文件位置：img/cursor/**

  **📄修改内容：替换鼠标指针，可制作自己喜欢指针哦~**

  **📃添加代码：资源文件名不变，查找替换CDN地址前缀即可**

```
  cursor:url(https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cursor/ayuda.cur),auto
  cursor:url(https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cursor/work.cur),alias
  cursor:url(https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cursor/texto.cur),auto
  cursor:url(https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cursor/normal.cur),auto
  cursor:url(https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cursor/No_Disponible.cur),auto;
  cursor: url(https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cursor/ayuda.cur),auto !important;
  cursor:url(https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cursor/No_Disponible.cur),auto;
  cursor:url(https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cursor/No_Disponible.cur),auto;
  cursor:url(https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cursor/No_Disponible.cur),auto
  cursor:url(https://cdn.jsdelivr.net/gh/liufg520/Hexo-Sakura-CDN/img/cursor/texto.cur),auto
```

## 18.添加动态404页面

**📜404.html文件位置：Hexo根目录/source/404.html**

**📜404页面CDN资源文件位置：404文件夹**

  **📄404.html文件修改：将CDN前缀地址替换成你自己的。**

  **📂404目录文件替换：将img目录下的图片替换成你自己的，文件名不变。**

  **📃修改404.html代码：可修改**