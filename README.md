# JPress
![](http://7xv9xp.com1.z0.glb.clouddn.com/1.png)


## 简介
JPress，一个wordpress的java代替版本，使用JFinal开发。支持类似wordpress的几乎所有功能，比如：模板，插件等。同时在模板上，JPress提出了“模板即模型”的概念，方便模板制作人灵活制作业务模型，移除了widget等繁杂功能，同时在模板和插件制作上比wordpress更加灵活简洁。

但是，JPress又不是wordpress的java版本，它天生融合了微信公众平台，整合了国内众多云平台、短信发送、邮件发送平台，独创的“模板即模型”概念是wordpress所不具备的，只有资深的wordpress玩家才能体会里面的微妙关系。同时后续会添加微信文章同步，QQ公众平台，今日头条，一点资讯等新媒体的文章同步功能，更加国产和本地化。

## 在功能方面
*  支持自定义模型，自定义模型通过模板来定义，而不是后台功能。同时模型内容支持自定义类别，比如文章模型支持专题、分类、标签等类别。
* 支持多模板引擎，默认使用Freemarker，模板制作者可以使用其他引擎比如thymeleaf来渲染，同时支持后台在线编辑模板（目前暂时只支持freemarker引擎）。
* 支持多数据库类型，可以配置不同的数据库（目前暂只支持mysql）。
* 支持多编辑器，后台可视化编辑和markdown编辑自由切换，默认支持在线图片编辑和代码高亮等功能。
* 支持插件化，几行代码就可以完成一个插件的开发，git.oschina.net和github上已经有插件的helloworld实例。
* 支持自定义URL，网站内容URL风格自定义。
* API支持，方便APP或其他第三方调用数据。
* 国际化支持，使用JPress轻松制作任何语言的网站。
* 极简的SEO功能，可以为每篇文章、每个分类、每个标签单独设置SEO，支持sitemap输出。
* 用户注册支持邮件和短信验证，目前短信服务商暂时只支持阿里大鱼。
* 支持CDN设置，包括七牛，阿里云，又拍云等。
* 上传图片支持水印设置，同时上传图片自动剪切成为模板需要的多种图片尺寸，保证图片显示不会拉伸。
* 用户登录支持第三方登录，支持QQ、微信、微博、开源中国、github、Facebook、twitter、linkedin（目前只完成QQ、微信、微博、开源中国、github的登陆）。



## 在微信方面

* 支持微信菜单设置。
* 支持自动回复，添加关键字和回复内容。
* 支持默认回复，包括：用户关注时、进入多客服时、退出多客服时、发送图片时、发送语音时、发送视频时、发送位置时、发送连接时、用户扫描了带参数的二维码时、用户摇一摇时。
* 所有的自动回复或默认回复支持“高级回复”功能，比如回复一篇文章，回复一个网址…高级回复是由JPress内置开发的特殊回复，但完全可配置，今后会增加更多的“高级回复”功能。
* 自动回复或默认回复支持插件回复，调用JPress插件完成回复。
* 支持文章搜索，回复关键字即可返回关键字匹配文章。
* 未来会支持文章同步或微信导入等实用功能。


## 在技术方面
* 自豪的采用了JFinal作为核心，JPress也是得益于JFinal灵活的架构。在JFinal framework开源体系里，JPress关心每行逻辑的实现，重视每行代码质量，应该属于JFinal的最佳实践，所以也应该是每个JFinaler必读的项目。
* 使用Freemarker和thymeleaf作为模板引擎。JPress内置的独创缓存，使得的UI渲染速度已经和模板引擎无关。
* 使用了tinymce做可视化编辑器，使用simplemde做markdown编辑器。两者可以后台自由切换。
* 文件和图片上传的UI插件使用了fine-uploader。
* 在前端上，JPress使用了jquery，bootstrap，admin lte，font-awesome，x-editable，fastclick，toastr，tag-editor，pace，layer等。
* 在安全方面，尽管我个人做了非常多的努力，已经在XSS，CSRF，SQL注入，Cookie安全等方面做了很多的工作，但是还是需要更多的人来一起挖掘和完善，安全是一个永恒的话题。（但是对于新手朋友来说，这些安全应该都是值得去学习和了解的，不是吗？）
* 支持分布式部署，JPress重写了HttpSession，使用ehcache实现了session的功能，同时在项目中大量依赖于cookie，在分布式架构上毫无压力。

## JPress有以下特点
#### 1、 轻。

>轻到只有 **8张** 数据表，却能实现wordpress的几乎所有功能。依赖的jar包也极度轻，目前只有cos-26Dec2008.jar、druid-1.0.16.jar、ehcache-2.7.5.jar、fastjson-1.2.7.jar、freemarker-2.3.23.jar、javax.mail.jar、jfinal-2.2-bin-with-src.jar、jfinal-weixin-1.7-bin-with-src.jar、jsoup-1.8.3.jar、log4j-1.2.17.jar、mysql-connector-java-5.1.36.jar、slf4j-api-1.7.7.jar、slf4j-log4j12-1.7.7.jar、jetty-server-8.1.8.jar 这 **14个** jar包，而且其中jetty-server-8.1.8.jar 不是必须的，只用于方便调试。<br /> 包括jar包在内的整个项目在20MB左右。

#### 2、 快。

>无论多么复杂的页面，JPress响应几乎在10毫秒内，同时JPress支持阿里云，七牛，又拍云等CDN作为加速，支持分布式部署等功能，就算是香港的服务器，只能用“飞快”来形容。

#### 3、灵活。

>JPress提出的“模板即模型”的概念，模板制作人可以用JPress来做博客，新闻系统，论坛，问答社区，商城…加上其灵活的插件功能，几乎可以用来做任何类型的网站。

#### 4、国产。

>因为国产，所以更符合国人需求。JPress天生融合了微信公众号，JPress内置了 阿里大鱼 的短信发送功能，支持了QQ邮箱，163邮箱等作为邮件发送服务器，后续会增加微信模板消息发送通知用户等更加符合国人需求的功能。


## 最最重要的的是
JPress使用了最宽松的LGPL开源协议，和国内的那些采用了 **私有协议** 的“开源”产品并不是一个级别的。

###最后来几张截图
![](http://7xv9xp.com1.z0.glb.clouddn.com/1.png)
![](http://7xv9xp.com1.z0.glb.clouddn.com/2.png)
![](http://7xv9xp.com1.z0.glb.clouddn.com/3.png)
![](http://7xv9xp.com1.z0.glb.clouddn.com/4.png)
![](http://7xv9xp.com1.z0.glb.clouddn.com/5.png)
备注：第二套模板（the3）还不完善，如果要做网站请使用第一套模板 或者 自行设计一套模板。

### 目前我在 [全职] 开发JPress，如果您觉得这个产品对您有用，您可以捐助下我，让我有理由继续下去，非常感谢。
![](http://7xv9xp.com1.z0.glb.clouddn.com/zz.jpg)


### 非常感谢以下朋友的捐助：

| 名字      | 金额   | 方式  | 说明  | 时间  |
| :-------: |:----: | :-----:|----- |-----|
| 我(enj***@gmail.com) | ￥30.00  | 支付宝捐助   | 祝jpress越来越好！ | 2016-6-13 19:03|
| 勐萌      | ￥6.66  | 微信捐助   | 无 | 2016-6-13 18:01|
| 盛宇伟    | ￥2.00  | 微信捐助   | 无 | 2016-6-13 15:41|
| Dean     | ￥10.00 | 支付宝捐助  | 简单支持下 | 2016-6-13 12:53|
| 花无雨    | ￥20.00 | 微信捐助   | 无 | 2016-6-13 11:23|
| 灿灿宝宝  | ￥18.88  | 支付宝捐助 | 要养老婆孩纸，没财权，支持jpess下 | 2016-6-13 11:01|



### 您也可以加入JPress交流QQ群：288397536 ，欢迎给我提建议和bug。<br >或者给我邮件：fuhai999@gmail.com 
