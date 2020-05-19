```diff
+ cache
  enable:true
+ since: 
+ scheme: Gemini
+ menu:自己设置
+ menu_settings:
  icons: true
  badges: true
+ avatar:
  url: /images/avatar.jpg
  rounded: true
  rotated: true
+ social:自己设置
+ links:自己设置
+ reward_settings:
  enable: true
  animation: true
+ reward:
  wechatpay: /images/wechatpay.png
  alipay: /images/alipay.png
+ follow_me:自己设置
+ codeblock
  copy_button:
    enable: true
    show_result: true
+ reading_progress:
  enable: true
+ pjax: true
+ mediumzoom: true
+ lazyload: true
+ pangu: true
+ vendors:
  pjax:  //cdn.jsdelivr.net/gh/theme-next/theme-next-pjax@0/pjax.min.js
  mediumzoom:  //cdn.jsdelivr.net/npm/medium-zoom@1/dist/medium-zoom.min.js
  lazyload:  //cdn.jsdelivr.net/npm/lozad@1/dist/lozad.min.js
  pangu:  //cdn.jsdelivr.net/npm/pangu@4/dist/browser/pangu.min.js
  disqusjs_js:  //cdn.jsdelivr.net/npm/disqusjs@1/dist/disqus.js
  disqusjs_css:  //cdn.jsdelivr.net/npm/disqusjs@1/dist/disqusjs.css
+ comments:
  active: valine #自选
  lazyload: true
+ valine:
  enable: false
  appid: # Your leancloud application appid
  appkey: # Your leancloud application appkey
+ local_search:
  enable: true
  trigger: manual
+ chat:
  enable: true
  service: chatra #自选
+ chatra:
  enable: true
  async: true
  id:  # Visit Dashboard to get your ChatraID
- github_banner:
  enable: false
- bookmark：false
```
所有用到的静态图片得放在`next`主题目录下的`source\images`目录中

 //cdn.jsdelivr.net/gh/jquery/jquery@3.2/dist/jquery.min.js
 //cdn.jsdelivr.net/gh/longer008/images@1.0/2020/vip/2020-04-12_11-09-01.png

修改`valine.svig`中的`{%- set valine_uri = theme.vendors.valine or '//unpkg.com/valine/dist/Valine.min.js' %}`为`{%- set valine_uri = theme.vendors.valine %}`



查看release之后的文件：

```
https://cdn.jsdelivr.net/gh/longer008/longer008.github.io@2.0/
```

给本地 js文件添加cdn服务：

修改`next/sripts/helpers/engin.js`文件

```diff
+ return urls.map(url => this.js(`https://cdn.jsdelivr.net/gh/longer008/longer008.github.io@2.0/${js}/${url}`)).join('');
- return urls.map(url => this.js(`${js}/${url}`)).join('');
+   return this.url_for(`https://cdn.jsdelivr.net/gh/longer008/longer008.github.io@2.0/${internal}/${url}`);
- return this.url_for(`${internal}/${url}`);
```

