###### [查询网站所选择的操作系统检验网址:www.netcraft.com](http://www.netcraft.com)

### 软件的分类

    网络软件分为两种，Cs/Bs。
        CS结构:是客户端（Client）与服务器（Server）端进行通信的网络软件,他们之间需要有特定的界面。
        BS结构:是浏览器(Browser)与服务器(Server)之间的通信协议软件，他们靠HTTP协议进行通信
            web模式就是输入BS模式的软件。
            BS模式的优缺点:
                1.维护和升级方便。
                2.成本较低，选择更多。
                3.应用和服务器的负载较重
                4.可以控制用户使用的所有版本，不需要用户手动更新
            BS软件的最大的优点就是可以在任何地方进行操作而不需要安装专门的软件，只要有一台能上网的电脑就能使用，客户端零维护，系统的扩展非容易
### HTML发展史

    1983    IETF发布了HTML1.0版本
    1995    w3c 接管  发布了HTML2.0
    1996    w3c 发布了HTML3.2版本（很多  很乱)
    1997    W3C发布了HTML4.0版本（精简版）
    1999    w3c 发布了HTML4.01版本（普通使用版本）；
        这是开始分路 
        线路1：xhtml版本
            2000年        W3C发布了XHTML1.0版本
            2001年        XHTML1.1
            W3C准备       XHTML2.0版本。夭折了
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

### 序列标签
```html
    <!--无序，顺序前面显示小圆点。-->
    <ul>
        <li>第一项</li>
    </ul>
    			
    <!--有序列表，顺序前面有顺序的显示	，新增reversed单属性，使顺序倒叙。-->
    <ol reversed>	
        <li>第一项</li>
    </ol>
    
    <!--ul和ol的子标签-->
    <li></li>
    
    <!--定义列表项目-->
    <dl>
        <dt>
            <dd></dd>
        </dt>
    </dl>
    	
    <!--定义一个列表中的一个项目-->
    <dt>
        <dd></dd>
    </dt>
    			
    <!--对项目中的描述，以及dialog中的聊天标签、-->
    <dd></dd>
    
    <!--原格式输出-->
    <pre></pre>		
    <pre>这 里  的内容  全部   原格式输入。包括空格     </pre>
    
    <!--换行标签-->
    <br/>
```

### 超链接标签
```html
<!--超链接标签-->
    <a></a>
    <!--
        a标签是一个超级链接标签，从这个页面链接到另外一个页面。
        常用的属性:
            href="URL/文件路径"	href属性代表需要链接的地址或文件路径
            taergt="_black"		target 打开链接的方式，_black新窗口打开。
    -->

    <!--举例:-->
    <a href="http://www.baidu.com" target="_black">在新窗口打开百度首页</a>
    
    <!--锚点举例:-->
    <a href="#come">你在哪</a>
    <a id="come">我在这</a>
    
<!--使用a链接发送邮件-->
    <a href="mailto:123@qq.com?cc=456@qq.com,多个人的邮箱,多个人的邮箱,&bcc=789@qq.com&subject=主题内容&body=邮件内容">点击发送邮件</a>
    <!--
        mailto:     收件人
        ?cc         抄送人
        &bcc        密送人
        &subject    邮件主题
        &body	    邮件内容
        mailto	    收件人
        注意：：如果要同时发送给多个人，那么邮箱地址后面用英文状态下的逗号分隔 
    -->
```

### 进度条标签
```html
<!--
一般用于进度的过度
属性：
    low	    最小警告值	内置红色
    high	良警告值	    内置黄色
    optimum	优秀		    内置绿色
    min	    最小值
    max	    最大值
    value	当前值
-->

<progress min="0" max="100"  value="10"></progress> 

<!--一般用于强度检测-->
<meter low="10" high="80" optimum="100" min="0" max="100" value="50"></meter>
```

### 多媒体标签
```html
<!--
定义图片资源的标签
属性：
    src="./xxx.png"		需要连接的图片地址
    width="900px"		设定图片的宽度
    height="300px"		设定图片的高度
    alt="图片不在"		如果图片不在
    title="鼠标显示文字"	鼠标放上去显示的文字
    ismap	            单属性，需要配合a标签来使用。把鼠标点击图片坐标传到服务器
-->
<img src="./image/aaa.png" width="100px" height="300px" alt="图片不在"  title="鼠标放上来" />

<!--
音频标签
    属性：
        controls	    用来开启播放器
        loop		    重复播放
        Autoplay	    自动播放
        src		        资源的地址（不推荐使用）
-->         
<audio controls loop>
    <!--source 为子标签，可以定义多个-->
    <source src="./a.mp3" />
    <source src="./a.mp3" />
    <source src="./a.mp3" />
</audio>

<!--
视频标签
    属性：
        controls	开启播放器
        loop		重复播放
        poster		播放视频前显示的图片
        width		视频的宽度
        height		视频的高度
        autoplay	自动播放
        src		    视频的地址（不推荐使用）
-->
<video poster="./img/a.png" controls loop width="" height="">
    <!--source 为子标签，可以定义多个-->
    <source src="./a.mp4" />
    <source src="./a.mp4" />
    <source src="./a.mp4" />
</video>

<!--
加载多媒体 一般用它加载flash
属性：	
     width		宽度
     Height		高度
     Src		flash地址
 --> 
<embed></ember>
```