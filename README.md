###### [查询网站所选择的操作系统检验网址:www.netcraft.com](http://www.netcraft.com)

### 软件的分类

    网络软件分为两种，Cs/Bs。
        CS结构:是客户端（Client）与服务器（Server）端进行通信的网络软件,他们之间需要有特
        定
        的界面。
        BS结构:是浏览器(Browser)与服务器(Server)之间的通信协议软件，他们靠HTTP协议进行通
        信
            web模式就是输入BS模式的软件。
            BS模式的优缺点:
                1.维护和升级方便。
                2.成本较低，选择更多。
                3.应用和服务器的负载较重
                4.可以控制用户使用的所有版本，不需要用户手动更新
            BS软件的最大的优点就是可以在任何地方进行操作而不需要安装专门的软件，只要有一台能上网的电脑就能使用，客户端零维护，系统的扩展非容易
### HTML发展史

    1983  IETF发布了HTML1.0版本
    1995  w3c 接管  发布了HTML2.0
    1996 w3c 发布了HTML3.2版本（很多  很乱)
    1997  W3C发布了HTML4.0版本（精简版）
    1999 w3c 发布了HTML4.01版本（普通使用版本）；
        这是开始分路 
        线路1：xhtml版本
            2000年  W3C发布了XHTML1.0版本
            2001年     XHTML1.1
            W3C准备XHTML2.0版本。夭折了
        线路2:HTML5版本 
            HTML5版本 所有的浏览器厂商一起研发的。
            HTML5在1999-已经发布草案
            2004-2008 W3C和whatwg合并了
            2008 W3C和whatwg HTML5正式版本（只是制定，并没有发布）
### 9.创建html文档

    文档的命名规则
        1.不允许使用特使字符
        2.可以使用中文，但不推荐使用。
        3.以.html 或 .htm为文件名。文件名推荐使用小写。
        
### html主题文档

```html
<!--在html文档中的第一行写上这句。意思是告诉浏览器以html5的规范解析-->
<!DOCTYPE html>
<html>
    <head>
    
    </head>
    
    <body>
        <!--网站内容在 body结构中-->
    </body>
</html>
```

### html头部元素 head
```html
    <!--标签为页面上的所有链接规定默认地址或默认目标。-->
    <base href="http://www.w3school.com.cn/i/"/>
    <base target="_blank"/>
    
    <!--设置字符编码-->
    <meta charset="utf-8" />
    
    <!--设置网站关键字-->
    <meta name="keyword" content="网站关键字，多个关键字使用逗号分隔" /> 
    
    <!--设置网站描述-->
    <meta name="description" content="网站描述内容" />
    
    <!--设置网站作者。-->
    <meta name="author" content="写上作者" />
    
    <!--网页自动刷新，页面跳转-->
    <meta http-equiv="refresh" content="5" />
    <meta http-equiv="refresh" content="5; url=http://www.baidu.com" />
    
    <!--设置网站标题-->
    <title>网站的标题</title>
    
    <!--标签,定义两个文档之间的链接-->
    <link />
    
    <!--引用外部CSS文件-->
    <link rel="stylesheet" type="" href="./css/index.css" />
    
    <!--设定浏览器ico小图标  所有类型的图片都可以 -->
    <link rel="icon" href="./image/a.ico" />
    
    <!--引用JS文件两种方法-->
    <script>
        <!--js脚本-->
    </script>
    <script src="./js/index.js" type="javascript" ></script>
 ```
 
### 文本标签 
```html
    <!--文本段落标签。会自动换行，自动占据一行-->
    <P></p>
    
    <!--文本加粗-->
    <b></b>
    
    <!--强调粗体。和粗体无区别。无须在意，快被遗丢的标签-->
    <strong></strong>
    
    <!--斜体文本-->
    <i></i>
    
    <!--强调斜体-->
    <em></em>
        <!--了解:
            B标签是物理标记，strong是逻辑标记
            什么是物理标记
                B是 bold加粗的简写，传递的意思就是加粗
            什么是逻辑标记
                Strong 是强调的意思，强调某个字段 -->
                
    <!--家族标签有 h1 ~~ h6的标签，没有h6以下的标签 一般用于定义标题。-->
    <hn></hn>
    
    <!--定义为下标文本-->
    <sub>2</sub>
    
    <!--定义上标文本-->
    今天天气有23<sup>°</sup>
   
   <!-- 把文本反向显示。颠覆文本的顺序默认是  ltr left到right 属性有 rtl right到left-->
    <bdo dir="rtl">赵兄托我办点事</bdo> 
   
   <!--定义元素细节 注意这个和form表单中的datalist很像。注意不要记忆混淆。 -->
    <details>
        <summary>电影名称</summary>
            <p>
                电影名称:奔跑吧,兄弟!<br/>	
                票价:60<br/>	
                评价:搞笑，大爱~~<br/>	
            </p>
    </details>
               
    <!--聊天标签-->
    <!--注意:在dialog中写上open="true" 方能显示效果。chrome有效-->
    <dialog open="true">
        <dt>在吗</dt>
            <dd>不在</dd>
        <dt>在吗</dt>
            <dd>不在</dd>
    </dialog>
```