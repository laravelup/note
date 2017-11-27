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
### 创建html文档

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
        //js脚本
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

### 表格标签
```html
<table></table>
<!--
属性:
    border			设定表格的边框
    width			表格的宽度
    height			表格的高度
    background		背景图像
    ......		
--> 
<!--字标签-->
    <!--定义表格的标题，通常配合<h1></h1>一起使用-->
    <caption></caption>	
    
    <!--表格的头部-->
    <thead></thead>		
    
    <!--表格的内容-->
    <tbody></tbody>		
    
    <!--表格的底部-->
    <tfoot></tfoot>		
    
    <!--定义表格的表头,会自动居中并且加粗。-->
    <th></th>		
    
    <!--定义表格的行数，横排数量。-->
    <tr></tr>	
    	<!--
            属性：
                center	内容居中配合align使用
        --> 
            
    <!--定义表格的列数，竖排数量。-->
    <td></td>	
    	<!--
            属性：
                rowspan	需要合并的行数，跨行 竖着的
                colspan	需要合并的列数，跨列 横着的
        --> 
<!--小例子-->
<table border="1px" width="800px">
    <caption><h1>学员信息表</h1><caption>
    <thead>
        <tr>
            <th>姓名</th>
            <th>性别</th>
            <th>年龄</th>
        </tr>
    </thead>
    
    <tbody>
        <tr>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
    </tbody>
    
    <tfoot>
        <tr>
            <td colspan="3" height="80px"></td>
        </tr>
    </tfoot>
</table>
```

### 表单标签
```html
<form></form>
<!--
属性:
    action		用于提交到服务器的页面
    method		提交的方法 GET POST 、、、等
    enctype		设定表单传输的数据类型，一般在上传文件的时候会使用到。
-->
<!--子标签-->
    <input type="text" />
    <!--    type属性值列表
            text		    文本框
            password	    密码域，输入时会出现星号代替。
            radio		    单选框,在name中需要写上相同的值，做排斥作用
            checkbox	    复选框,同上的name写法
            hidden		    隐藏表单,在浏览器中不会显示任何效果。
            file		    文件上传表单,加上multiple时是多文件上传，name加上[]
            reset		    清空表单，把当前填写的内容全部清空。
            image		    图片上传按钮，当中有Src的属性，链接图片地址。
            button		    普通按钮，也可以作为提交。
            submit		    提交按钮，在value中写上文字即可。
            email		    邮箱表单,验证写入的是否是邮箱
            Url		        URL验证，必须是完整的URL地址才行。
            color		    颜色选择表单，方便快捷
            Tel		        电话表单，在手机端可以出现效果
            number		    数值表单
            range		    滑块表单，一般用于数量上的选取
            search		    搜索表单，在里面写上results="n" 会显示放大镜
            date		    时期选取
            time		    时间选取
            week		    周选取，一选就是一个周
            month		    月选取，一选就是一个月
            datetime	    完整时间---目前没有任何效果
            datetime-local	本机时间。完整的 
    -->
    
    <button type="button"></button>  
    <!--type属性值列表
            reset		    清空表单，把当前填写的内容全部清空。
            button		    普通按钮，也可以作为提交。
            submit		    提交按钮，在value中写上文字即可。
    -->
    
    <select name="">
        <!--普通下拉框-->
        <option value=""></option>
        
        <!--下拉框类分组：-->
        <optgroup label="分组项">
            <option>小组1</option>
        </optgroup>
    </select>
    
    <!--大文本域-->
    <textarea cols="" rows="">内容写在这里</textarea>
        
    <!--绑定标签-->
    <label></label>
    
    <!--标签分组-->
    <fieldset>
        <legend>性别选择</legend>
        <label for="">男：<input type="radio" name="sex" value="1" /></label>
        <label for="">女：<input type="radio" name="sex" value="0" /></label>
    </fieldset>
    
    <!--模仿百度搜索的下拉效果-->
    搜索：<input type="search" name="so" list="so" />
    <datalist id="so">
        <option>手机</option>
        <option>电脑</option>
        <option>平板</option>
    </datalist>
    <!--注意:在搜索标签中绑定list，在datalist中写上ID值，即可完成下拉效果。在datalist中加上子标签 <option>下拉值</option>即可完成-->

    <!--单选/复选点击文字即可选中效果 --需要把label中的for属性值去除-->
    <label>男：</input type="Radio" name="sex" value="1" /></label>
    <label>女：</input type="radio" name="sex" value="0" /></label>
    <label>复选1</input type="checkbox" name="mult" value="d[]" /></label>
    <label>复选2</input type="checkbox" name="mult" value="d[]" /></label>
    
    <!--form标签与input分离-->
    <form action="" method="GET" id="form"></form>
    <input type="text" name="username" form="form" />
<!--
    在HTML5中新增的type属性与值
    readonly		输入域可以选择，但是无法修改
    disabled		无法获取到焦点,呈现灰色状态。
    autofocus		自动获取焦点，这是个单属性
    placeholder=""	代替文本的value值，且不会被提交，颜色表浅。
    pattern="\d+"	正则验证输入的内容
    step=""			跳过的数量，可以用在number数值中。
    required		强制用户输入的项目。
    min			    最小值，一般可以用于滑块，数值，时间。
    max			    最大值。一般可以用于滑块，数值，时间。
    novalidate		取消验证，不验证。可以写在form表单中
    formaction		改变提交的地址，写在submit写在那个表单中
    formmethod		改变提交的方式，写在submit写在那个表单中
    Formectype		改变提交文件的数据类型。同上
    formnovalidate	取消验证，不做验证。同上
-->			
```

### 框架标签

```html
<!-- 基本上已废弃-->
<frameset>

<!--
属性:
    src         目标地址
    frameborder 边框
    cols	    分配行		X轴
    rows	    分配列		Y轴
    Noresize    none        禁止页面拖动。
-->
<iframe></iframe>
```


### Css
##### 基本选择器

    1.类选择器
        格式：
            <style>
                .p1{样式}/*在style前面写上.*/
            </style>
            <p class="p1">这个是类选择器的定义</p> 
            
    2.标签选择器
        格式：
            <style>
                p{样式}/*直接写上标签名*/
            </style>
            <p>这个是标签选择器</p>
    3.ID选择器
        格式：
            <style>
                #a{样式}/*加上#号*/
            </style>
            <p id="a">这个是标签选择器</p>
    4.通配符选择器
        格式:
            *{样式}/*定义所有html文档*/
            
##### 层级选择器

    1.包含选择器 E E2 / E > E2
        格式:
            <style>
                p a{样式}/*两个元素之间使用空格分隔*/
                p > a{样式}/*用法和功能一样*/
            </style>
            <p>
                <a></a>
            </p>
    2.组合选择器 E,E2
        格式：
            <style>
                h1,p{样式}/*使用英文逗号分隔*/
            </style>
            <h1></h1>
            <p></p>
    3.E + E2 选择器 选择+号后面第一个标签
        格式：
            <style>
                div + h1{样式}/*这个只会选中一个，也就是第一个H1*/
            </style>
            <div></div>
            <h1>选择这个</h1>
            <h1>选不中</h1>
            <h1>选不中</h1>
            <h1>选不中</h1>
    3.E ~ E2 选择器
        格式:
            <style>
                div ~ h1{样式}/*全部选中E 标签后面的兄弟元素*/
            </style>
            <div></div>
            <h1>全部选中</h1>
            <h1>全部选中</h1>
            <h1>全部选中</h1>
            <h1>全部选中</h1>

##### 属性选择器
    属性选择器就是根据属性名或是属性值来找到元素 ATT表示属性名 VAL代表属性值
    1.E[ATT]
        匹配标签中的属性名，不考虑属性值，如果不加上E则只会匹配ATT
        格式：
            <a href="http://www.baidu.com">百度</a>
            <style>
                a[href]{样式}
                /*下面是不写标签名*/
                [href]{样式}
            </style>
    2.E[ATT='val']写值的时候请加上单引号''
        匹配ATT中的值一样，如果不一样匹配不到
        格式：
            <a href="http://www.baidu.com">百度</a>
                <style>
                    a[href='http://www.baidu.com']{样式}
                </style>
    3.E[ATT ~= 'val']
        匹配ATT的值如果有就能匹配的到就是约等于就行。
        格式：
            <a href="http://www.baidu.com">百度</a>
                <style>
                    a[href ~= '//']{样式}
                </style>
    4.E[ATT |= VAL]
        匹配所有ATT属性具有多个连接分隔符的值，匹配-前的第一个值
        格式：
            <h1 title="ab-cd-ef">横杆分隔符选择器</h1>
                <style>
                    a[title |= 'ab']{样式}
                </style>
    CSS3用到的属性选择器
    5.[ATT ^= VAL]
        匹配ATT的val开头的元素
        格式：
            <h1 title="ab cd ef">匹配第一个值</h1>
                <style>
                    a[title |= 'ab']{样式}
                </style>
    6.[ATT $= VAL]
        匹配val的结尾值
        格式:
            <h1 title="ab cd ef">匹配第一个值</h1>
                <style>
                    a[title |= 'f']{样式}
                </style>
    7.[ATT *= VAL]
        匹配VAL的值只要有就行
        格式：
            <h1 title="ab cd ef">匹配第一个值</h1>
                <style>
                    a[title |= 'f']{样式}
                </style>

##### 结构伪类选择器
    伪类选择器不是真的类选择器，是对没有标签的内容增加样式。
    E:First-line	E元素的第一行
        格式:
            <style>
                li:forst-line{样式}
            </style>
            <ul>
                <li>1</li>
                <li>2</li>
                <li>3</li>
                <li>4</li>
            </ul>
    E:first-letter	E元素的第一个字母
        格式：	
            <style>
                li:forst-line{样式}
            </style>
            <ul>
                <li>1</li>
                <li>2</li>
                <li>3</li>
                <li>4</li>
            </ul>
    E:Before	E元素之前
        p:before{
            content:"这是放P之前";
        }
    E:after		E元素之后
        p:after{
            content:"this is a test";
        }
