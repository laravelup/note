###### [查询网站的操作系统](http://www.netcraft.com)

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
        mailto      收件人
        cc          抄送人
        bcc         密送人
        subject     邮件主题
        body	    邮件内容
        如果要同时发送给多个人，那么邮箱地址后面用英文状态下的逗号分隔 
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


### Css篇
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

    1.包含选择器 E E2 or E > E2
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

##### 其它选择器

    E:first-child
        选择元素的正序第一个
        格式:
            <style>
                li:first-child{样式}
            </style>
            <ul>
                <li>1</li>  <!-- 这个被选中 -->
                <li>2</li>
                <li>3</li>
            </ul>
    E:last-child
        选择元素的倒序第一个
        格式:
            <style>
                li:last-child{样式}
            </style>
            <ul>
                <li>1</li>
                <li>2</li>
                <li>3</li>  <!-- 这个被选中 -->
            </ul>
    E:nth-child()
        正序选择，可以输入数字，正数不能输入负数,这个不会跳过。
        格式:
            <style>
                li:nth-child(2){样式} /*如果选择3则不会有任何变化*/
            </style>
            <ul>
                <li>1</li>
                <li>2</li>      <!-- 这个被选中 -->
                <a>链接</a>   
                <li>3</li>
            </ul>
    E:nth-last-child()
        倒叙选择，可以输入数字，正数不能输入负数不会跳过。
        格式:
            <style>
                li:nth-child(3){样式}/*如果选择2则不会有任何变化
                */
            </style>
            <ul>
                <li>1</li>
                <li>2</li>          <!-- 这个被选中 -->
                <a>链接</a>
                <li>3</li>
            </ul>
    E:nth-of-type()
        正序选择，可以输入数字，正数不能输入负数,这个会跳过
        格式:
            <style>
                li:nth-child(3){样式}/*其实是最后一行增加样式*/
            </style>
            <ul>
                <li>1</li>
                <li>2</li>
                <a>链接</a>
                <li>3</li>
            </ul>
    E:nth-last-child()
        倒序选择，可以输入数字，正数不能输入负数,这个不会跳过
        格式:
            <style>
                li:nth-child(2){样式}/*不会有任何样式*/
            </style>
            <ul>
                <li>1</li>
                <li>2</li>
                <a>链接</a>
                <li>3</li>
            </ul>
    E:nth-last-of-type()
        倒序选择，可以输入数字，正数不能输入负数,这个会跳过
        格式:
            <style>
                li:nth-child(2){样式}/*其实是那个2增加样式*/
            </style>
            <ul>
                <li>1</li>
                <li>2</li>
                <a>链接</a>
                <li>3</li>
            </ul>
    E:nth-child(an+b)ａ表示循环跳过的层数，B表示循环起始的位置
        格式：
            <ul>
                <li>1</li>
                <li>2</li>
                <li>3</li>
                <li>5</li>
            </ul>
            <style>
                li:nth-child(2n+1){样式}/*只有第三行增加样式*/
            </style>
    E:only-chiled               匹配父元素仅有的一个子元素的
    E:only-of-type              匹配父元素下使用同种标签的唯一一个子元素
    [ATT=VAL]:enabled           匹配表单中激活的元素
    [ATT=VAL]:disabled          匹配表单中禁用的元素
    [ATT=VAL]:checked+n:        匹配表单中被选中的radio或checkbox元素
        格式：
            <input type="radio" name="" value="" /><a>男</a>
            <style>
                [type='radio']:checked+a{
                    background-color:red;
                }
            </style>
            
    ::selection 匹配用户当前鼠标选中的元素
        格式:
            ::selection{
                color:lime;
            }
##### 伪类选择器

    E:link		链接未被访问的样式
        举例:
            <style>
                a:link{
                    color:red;
                }
            </style>
            <a>百度</a>
    E:hover		鼠标放上去的样式
        举例:
            <style>
                a:hover{
                    color:pink;
                }
            </style>
            <a>百度</a>
    E:Visited	链接被访问的样式
        举例:
            <style>
                a:visited{
                    color:black;
                }
            </style>
            <a>百度</a>
    E:focus		获得焦点时候的样式
        举例:
            <style>
                input:focus{
                    background-color:red;
                    margin-left:600px;
                }
            </style>
            <input type="text" name="admin" value="" autofocus />
    E:target	到达目标后的样式
        举例:
            <style>
                #a:target{
                    margin-left:60px;
                }
            </style>
            <a href="#a">百度</a>
            <a id="a">移动</a>
        注意:在CSS中只可以写上目标值。否则不能增加样式
        
### 常用的属性

> ###### 字体属性

    Font-style 
        设置字体样式 
        常用属性值
            Normal 默认的
            Italic 斜体
            Oblique 斜体
        格式:
            <p style="font-style:italic">斜体文本</p> 

    Font-family   dacoration:none;
        用于设置字体的类型
        格式:
            <p style="font-family:微软雅黑">微软雅黑的字体</p>
        注意：页面中该属性设置的字体必须存在于客户端电脑中，才可以使用
    
    Font-size 设置字体大小
        常见的单位：
            Px:像素 屏幕中的一个点就是一个像素
            Em:一个汉字的大小 相对值
            Ex : 就是一个X字体的大小
            换算：1em=2ex（相对单位）
        格式：
            <p style="font-size:100px">100像素的字体</p>

    Font-weight 
        设置字体的粗细数值格式唯一有用的就一个800
        Bold 加粗
        默认值：normal
        格式:
            <p style="font-weigth:800">粗体为800</p>
    
    	Font-variant  
    		只对英文有效
    			Normal 正常字体
    			Small-caps 将小写字母变为小型的大写字母-----(不常用。)
    	Font 
    		字体样式统一设置---（不推荐使用）
    		注意：使用该属性时，值具有顺序关系，必须依照顺序来写，不存在的可以省略
    		Font属性顺序
    			斜体/小型大写字母/粗体/（字体大小/行高） 字体风格
    		格式:
    			<p style="font:Italic Small-caps 800 30/60 微软雅黑">一起来</p>
    
> ###### 文本属性

    Text-indent:
        首行缩进
    
    Line-height:
        用于设置单行文本的行高，就是一个的高度
            1.设置行间距（行高）用于美化效果
            2.用于单行文本的垂直居中（行高设置为元素高度即可）
        格式:
            <p style="border:1px solid red;line-height:60px;">有行高</p>
    Text-align:
        用于文字内容的水平居中属性有left  center right	
        格式:
            <p style="text-align:center;text-align:right;">居中文字</p>
        了解的属性：
                Word-spacing:设置单词的词间距
                Letter-spacing:设置字母之间的间距

> ###### 背景属性

    	background-color
    		设置背景颜色，可以设置英文单词作为颜色值，也可以设置#f123456 也可设置
    		rgb(25,25,25)
    		格式:
    			background-color:#123456;
    	background-image
    		设置背景图片，需要加上URL引入背景图。经常需要使用到
    		格式:
    			background-image:url(./image/a.png);
    	background-repeat
    		用于设定背景图像是否重复，可选值有 repeat-x(X轴重复) repeat-y(Y轴重复) no-repeat
    		不重复
    		格式:
    			background-repeat:no-repeat;/*不重复背景图像*/
    			background-repeat:repeat-x;/*x轴重复图像,横的重复*/
    			background-repeat:repeat-y;/*Y轴重复，竖的重复*/
    		注意，这个只有这几个属性。还有一个默认的。基本用不上
    	bakcground-position
    		一般多数用于设定网站上面的小图标，可以设定图片的坐标值，可以设定英文值:left righe 
    		center bottom top 这些值，一般是给两个值。当遇到一个值的时候是正中居中。自动
    		center
    		格式:
    			background-position:bottom right;/*最下面的右边*/
    			background-position:bottom left;/*最下面的左边*/
    			background-position:top rigth;/*最上面的右边*/
    			background-position:top left;/*最上面的左边*/
    			background-position:center;/**/
    			background-position:0px -157px;/*这样是设定小图片的左边值 常用的是这个*/
    		注意:如果写上两个单词属性的话，则会按照规定的来摆放。如果只写一个left 或right都会
    		居中，一般常用的是小图片的坐标值。在写坐标值的时候一定需要加上px 不然不可以使用。
    		重点记忆项目。
    	background-attachment（哎 抬 吃 们T）
    		设置背景图片是否滚动
    		常用的属性值:
    			Fixed	绑定页面，图片固定住，不会滚动
    			scrool	默认属性，图片会随着滚动而滚动。
    	background
    		一起设置所有的样式，并且没有顺序之分。多个属性之间使用空格分隔。记忆方便
    		格式:
    			background:red url(./a.png) no-repeat center; /*设置背景图 不重复 居中*/
    		
    		相加多少都可以，不需要加的属性就省略。没有顺序之分。
> ###### 尺寸属性

    width
        设定宽度，常用的单位是像素 PX  很常用。
        格式:
            <div style="width:100px;">经常用到的属性</div>
    min-width
        设定最小的宽度,不常用。
        格式:
            <div style="min-width:100px;">不常用</div>
    max-width
        设定最大的宽度,不常用。
        格式:
            <div style="max-width:100px;">不常用</div>
    max-height
        设定最大的高度，不常用
        格式:
            <div style="max-height:300px;">不常用</div>
    height
        设定高度的属性 常用的也是像素 PX 很常用。
        格式:
            <div style="height:100px;">常用</div>
    min-height
        设定最小的高度，很常用。当超过最小的高度时会自动拉宽。 很常用，一般用于在文字发帖
        格式:
            <div style="min-height:300px;">常用的属性</div>
            
> ###### 列表属性

    	list-style-type
    		属性值
    			none		把li前面的小圆点和数字去掉。ul 和ol都可以去掉
    			circle		把前面的小圆点变成空心圆。这些都不重要。重点就是none
    		格式
    			list-style-type:none;/*去掉前面的小圆点*/
    			list-style-type:circle;/*变成其它样式的小圆点*/
    
    	list-style-image
    		属性值
    			url		把li前面的小圆点用图片代替。
    		注意:如果同时出现type和image的话，那么image的优先级最高。
    		格式
    			list-style-image:url(./a.png);/*使用图片代替小圆点*/
    	list-style-position
    		属性值
    			Inside		在内容中增加样式，就是把所有内容包进去
    			Outside		在内容外增加样式，把所有内容放在外面。
    		格式
    			list-style-position:inside;/*这里定义好，在下面继续增加样式即可*/
    			border:1px solid red;/*可继续增加。*/
> ###### 定位属性

    	position设置元素的定位方式
    		属性值
    			Relative	相对定位  以自己的位置移动	
    			Absolute	绝对定位  以父元素进行移动，body也是父元素。
    			Static		默认属性
    		理解相对定位
    			相对定位就是根据自己前期所在的位置进行移动，需要给谁相对移动就在谁的CSS中
    			增加position:relative;然后写上相对移动的位置 px像素。
    			格式:
    				position:relative;
    				left:30px;/*意思就是相对自己当前的位置来向左移动30像素*/
    
    		理解绝对定位
    			绝对定位就是根据body的位置来进行移动。
    			格式:
    				position:absolute:
    				top:30px;/*意思就是根据body的位置来向下移动30像素*/
    		注意：
    			1.如果在父元素中写上了是相对还是绝对，在子元素中写上移动的位置。那么会一
    			起移动。
    			2.如果存在嵌套关系的标签，父元素设定了定位的类型，那么子标签会遵循父元素
    			的位置来进行移动，如果父元素没有设定定位的类型，那么子标签会遵循body的坐
    			标来移动。1.relative	以自己的位置相对定位 2.absolute	以父元素定位
    			，body也是父元素。
    		
    		
    	Z-index
    		设定多层元素的显示顺序，数值越大越在上面。最大的是999
    		格式
    			z-index:1;
    			z-index:999;
> ###### 布局属性

    	在学习布局属性之前，需要学习两个html标签，无意义标签<div></div><span></span> 这两个标签是
    	无任何意义的标签，DIV会自动占一行，span不会自动占据一行。div是块级元素，span是行内元素。
    	DIV占一行。span不会占一行。span没有宽高属性。通过CSS可以有。
    	display
    		设置元素的显示方式。可以将块级元素变成行内元素，行内元素变成块级元素。
    		常用的属性值:
    			inline		将元素变成行内元素显示
    			block		将元素变成块级元素显示
    			inline-block	同时具备行内元素和块级元素的属性，可以设置宽高属性。
    			None		设置元素显示不显示，不显示的话不会占据物理位置。
    	Table-cell 设定一个元素像表格的单元格一个样式(目的就是垂直居中）
    	Visibility 设置元素是否显示
    		属性：
    			Visible		设置元素显示（默认）
    			hidden		隐藏不显示。仅仅隐藏元素内容，会占据物理位置。
    	Overflow-x:设置水平方向溢出显示
    	Overflow-y:设置垂直防线溢出显示设定内容超出元素宽高的显示方式
    		常用的值：
    			Visible:超出部分仍然显示
    			Scroll:内容超出高度或者宽度将出现滚动条
    			Hidden:超出内容隐藏处理（超出的内容有可能会被截断）
    			Overflow:设置水平方向以及垂直方向溢出显示方式
    			Overflow：hidden ；会自动检索当前元素内的所有元素
    	float
    		属性：
    			left		设置元素向左边浮动
    			right		设置元素向右边浮动
    			top		设置元素向上边浮动
    			bottom		设置元素向下边浮动
    		格式：
    			float:left;	float:right;	float:top;	float:bottom;
    		注意：任何元素一旦使用float属性，那么他的DISPLAY属性将完全失效，均可以设置宽高，
    		效果类似于inline-block  就是任何元素一但设定了浮动属性，那么都是可以设定宽高的。
    	如果内层的元素被平浮动，外层元素如何查找高度？
    		1.直接将外层元素设置为指定的高度
    		2.使用overflow:hidden 检索当前元素的内部子元素
    		3.将外层元素设置浮动 和内层元素一起浮动。
    		4.Clear:用于清除其他元素的浮动属性对当前元素的影响，是在浮动元素的下面增加这个属
    		性
    	clear 用于清除其他元素浮动属性的影响、
    		属性:
    			left	清除左边元素的浮动
    			right	清除右边元素的浮动
    			both	清除所有浮动。（推荐使用）

> ###### 盒子模型

    margin	设置div的外边距的距离。
        属性:
            left	设置左边距的值
        格式:		margin-left:10px;
            
            right	设置右边距的值
        格式：		margin-rightt:10px;
            top	设置上边距的值
        格式：		margin-top：10px;
            bottom	设置下边距的值
        格式:		margin-bottom:10px;
    以上的都是单独设置，统一设置的格式有4中。
    
    分别是:
        margin:10px 20px 30px 50px;     -->上 右 下 左 的边距为10 20 30 50顺时针的顺序来定义
        margin:10px 20px 30px;	        -->分别设定上边距10px  左右边距20px   下边距30px
        margin:10px 20px;	            ->>上下 左右 的参数 同时设置
        margin:10px;		            ->>上下左右全部为10边距
        margin:0 auto;		            ->>上下左右全部为0边距 自动居中。auto

    padding	设置div的内边距的距离。
        属性:
            left	设置左内补白的值
        格式:		padding-left:10px;
            
            right	设置右内补白的值
        格式：		padding-rightt:10px;
            top	设置上内补白的值
        格式：		padding-top：10px;
            bottom	设置下内补白的值
        格式:		padding-bottom:10px;
    以上的都是单独设置，统一设置的格式有4中。
        padding:10px 20px 30px 50px;    -->上 右 下 左 的内补白为10 20 30 50。顺时针的顺序
        padding:10px 20px 30px;	        -->分别设定上内补白10px  左右边距20px   下边距30px
        padding:10px 20px;	            ->>上下 左右 的参数 同时设置
        padding:10px;		            ->>上下左右全部为10边距
        padding:0 auto;		            ->>上下左右全部为0边距 自动居中。auto
    注意:margin 和padding类似。padding不同的就是会自动撑大元素。同时可以很好的把padding内的内容很好的居中

> ###### 边框属性
    border 设定边框的属性。
        属性：
            border-color	设置边框的颜色	
            border-style	设置边框的样式---》实线还是虚线。
            border-width	设置边框的像素。
            border:		    统一设置边框的属性，没有顺序。
            
        border-left中具有以下子属性
            border-left-style:	        设置左边框的样式
            border-left-colore:	        设置左边框的颜色
            border-left-width:	        设置左边框的像素
        border-right中具有以下子属性
            border-right-style:	        设置右边框的样式
            border-right-colore:	    设置右边框的颜色
            border-right-width:	        设置右边框的像素
        border-top中具有以下子属性
            border-top-style:	        设置上边框的样式
            border-top-colore:	        设置上边框的颜色
            border-top-width:	        设置上边框的像素
        border-bottom中具有以下子属性
            border-bottom-style:	    设置下边框的样式
            border-bottom-colore:	    设置下边框的颜色
            border-bottom-width:	    设置下边框的像素

> ###### 其他属性

    Cursor:
        设定鼠标样式 pointer 小手 样式
        格式:
            cursor:pointer;
    Zoom:
        设定元素的缩放倍数  可大可小 能伸能缩
        格式：
            zoom:1.5;/*1.5倍放大图片*/
    Text-decoration:设定文本修饰
        常用的值
            Underline:下划线
            Line-through:删除线 贯穿线
            None：取消样式/*用于在A链接上面，删除A链接下的横线.*/
            
>
# PHP篇
