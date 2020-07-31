## 若图片显示不出来，请查看CSDN博客：https://blog.csdn.net/star_of_science/article/details/107712226 

# js_Window_BOM
js基础、函数、Window对象、BOM编程

# JavaScript
JavaScript可以使网页增加互动性，也可以对表单提交进行验证减轻服务器的负担，JavaScript是Ajax技术中的核心。
## JavaScript的基本结构
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731141408165.png)
## javascript脚本执行原理
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731141553526.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)
## JavaScript核心语法
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731141707775.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)
### 变量
声明变量的关键字：var   
注意：在JavaScript中所有类型都可以用var来声明，也可以把var省略
声明变量语法：
1、先声明变量，再给变量赋值

```javascript
var num;
num = 2;
```

2、声明变量的同时给变量赋值

```javascript
var num = 2;
```

3、同时声明多个变量并赋值

```javascript
var a=2,b=”abc”,c=5;
```

4、不使用var直接给变量赋值

```javascript
num = 2;
```

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript">
        var a;
        a = 3;
        document.write(a+"<br>");

        var b = 20;//声明变量的同时给变量赋值
        document.write(b+"<br>");

        var c= 2,d=25.6,e=true;
        document.write(c+"-"+d+"-"+e+"<br>")

        f="abc";//建议不要省略var
        document.write(f);
    </script>
</head>
<body>

</body>
</html>
```

### typeof运算符的使用
用于得到变量或值对应的类型返回值(注意：类型返回值是一个字符串)
语法： typeof(变量或值)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731142212919.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript">
        var a;
        var b = "hello";
        var c = true;
        var d =23;
        var e = new Date();
        document.write(typeof(a)+"<br>")
        document.write(typeof(b)+"<br>")
        document.write(typeof(c)+"<br>")
        document.write(typeof(d)+"<br>")
        document.write(typeof(e)+"<br>")
    </script>
</head>
<body>

</body>
</html>
```

### 运算符
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731142309621.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)
### 逻辑控制语句
1、If条件语句
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731142352880.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)

2、switch多分支语句
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731142600367.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)

3、循环结构
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731142612844.png)
循环中断：break、continue

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript">
        /*
            java中的：真(true)  假(false)
            javascript中的：真(true、非null、非0)   假(false、null、0)
         */

        var a = null;
        if(a){
            document.write("为逻辑真");
        }else{
            document.write("为逻辑假");
        }
    </script>
</head>
<body>

</body>
</html>
```

### 消息框和输入框
alert()：提示框
prompt()：输入框(能够获取用户的输入)

用法：
![](https://img-blog.csdnimg.cn/20200731142737636.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript">
        //提示框(输出)
        //alert("大家好！");

        //用户输入
        var name = prompt("请输入姓名","您的姓名写在此处");
        document.write(name);
    </script>
</head>
<body>

</body>
</html>
```

## JavaScript的使用方式
1、内嵌JS代码
在网页的<script>标签中编写JS代码

```javascript
<script type="text/javascript">
	Javascript代码
</script>
```

2、外部JS文件
在网页中引入外部的JS文件来使用
引入的语法：

```javascript
<script type="text/javascript" src="js文件的路径"></script>
```

如果js代码很少，可以使用简短缩写方式

```javascript
<input name="btn" type="button" value="弹出消息框" onclick="javascript:alert('欢迎你');"/>
```
my.js
```javascript
var a;
a = 3;
document.write(a+"<br>");

var b = 20;//声明变量的同时给变量赋值
document.write(b+"<br>");

var c= 2,d=25.6,e=true;
document.write(c+"-"+d+"-"+e+"<br>")

f="abc";//建议不要省略var
document.write(f);
```
引用外部js.html
```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript" src="js/my.js"></script>
</head>
<body>
    <input name="btn" type="button" value="弹出消息框" onclick="javascript:alert('欢迎你');"/>
</body>
</html>
```

# 函数
函数类似于Java中的方法，是完成特定任务的代码语句块
函数分为：系统函数、自定义函数
## 常用的系统函数
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020073114370651.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript">
        var a = "23";
        a = parseInt(a);
        document.write(a+1);
        document.write("<br>");

        var b = "26abc";
        b = parseInt(b);//从左边开始解析，遇到不能解析的字符就停止
        document.write(b);
        document.write("<br>");

        var c = "a24bc";
        c = parseInt(c);
        document.write(c);//输出NaN(not a number)
    </script>
</head>
<body>

</body>
</html>
```

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript">
        var a = "23";
        if(isNaN(a)){//a不是数字返回true   a是数字返回false
            document.write("a不是数字");
        }else{
            document.write("a是数字")
        }
    </script>
</head>
<body>

</body>
</html>
```

## 自定义函数
自定义函数是由自己定义函数，分为无参函数、有参函数
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731143739211.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)
函数调用一般和表单元素的事件一起使用，调用格式：事件名＝“函数名( )" 
例如：  onclick=”show()”
```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript">
        function show(){
            for(var i=1;i<=5;i++){
                document.write("hello world!<br>")
            }
        }
        function show2(num){
            for(var i=1;i<=num;i++){
                document.write("hello world!<br>")
            }
        }
    </script>
</head>
<body>
    <input type="button" value="输出5次helloworld" onclick="show()" />
    <input type="button" value="输出helloworld" onclick="show2(prompt('请输入次数'))" />
</body>
</html>
```
# BOM
Browser Object Model的缩写，简称浏览器对象模型
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731153007838.png)

window表示浏览器对象
history表示浏览器历史记录对象
document表示文档对象
location表示地址栏对象

window对象常用属性：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731153031522.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript">
        document.write("电脑屏幕的高度："+window.screen.height+"<br>");
        document.write("电脑屏幕的宽度："+window.screen.width+"<br>");
        //电脑屏幕的有效高度=电脑屏幕的高度-任务栏高度
        document.write("电脑屏幕的有效高度："+window.screen.availHeight+"<br>");
        document.write("电脑屏幕的有效宽度："+window.screen.availWidth+"<br>");
    </script>
</head>
<body>

</body>
</html>
```

常用事件：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731153104417.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)


window对象常用方法：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731153110561.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript">
        //点击“确定”返回真    点击“取消”返回假
        var result = confirm("确定要删除吗？");
        if(result){
            document.write("按了确定按钮");
        }else{
            document.write("按了取消按钮");
        }
    </script>
</head>
<body>

</body>
</html>
```

open()方法的使用：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731153117606.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript">
        window.open("9_Screen的使用.html","","height=300,width=300,left=200,top=200");
    </script>
</head>
<body>
    <input type="button" value="open打开窗口" onclick=" window.open('9_Screen的使用.html','','height=300,width=300,left=200,top=200')" />
</body>
</html>
```

定时函数：
setTimeout(“调用的函数”,毫秒数)：多少毫秒后执行函数
setInterval(“调用的函数”,毫秒数)：每隔多少毫秒执行一次函数

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript">
        function greet(){
            alert("帅哥美女们，晚上好！");
        }
        function startTimeout(){
            window.setTimeout("greet()",2000);
        }
        var interval;//存储interval定时对象
        function startInterval(){
            interval = window.setInterval("greet()",2000);
        }

        function deleteInterval(){
            window.clearInterval(interval);//移除定时对象
        }

    </script>
</head>
<body>
    <input type="button" value="setTimeout的使用" onclick="startTimeout()" />
    <input type="button" value="setInterval的使用" onclick="startInterval()" />
    <input type="button" value="移除setInterval" onclick="deleteInterval()" />
</body>
</html>
```

## 匿名函数
匿名函数就是指没有函数名的函数
匿名函数的两种写法：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731153148331.png)

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript">
        //窗体加载事件(方法一)
//        window.onload = function(){//匿名函数
//            alert("大家好！");
//        }

        function greet(){
            alert("大家好！");
        }
        //窗体加载事件(方法二)
        window.onload = greet;//注意：greet后面不要加小括号

        var m = function(){
            alert("大家好！");
        }
    </script>
</head>
<body>
    <input type="button" value="问候" onclick="m()" >
</body>
</html>
```
## Date日期的使用
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731160558330.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)
日期各个单位的取值范围如下：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731160602773.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731160623771.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)
getYear()：获取当前年份与1900年相差的年份数
getFullYear()：获取当前年份

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript">
        var date = new Date();//创建当前日期对象
        document.write(date.getFullYear()+"<br>");
        document.write((date.getMonth()+1)+"<br>");
        document.write(date.getDate()+"<br>");
        document.write(date.getHours()+"<br>");
        document.write(date.getMinutes()+"<br>");
        document.write(date.getSeconds()+"<br>");
    </script>
</head>
<body>

</body>
</html>
```
## document的使用
document常用属性：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731161138550.png)
document常用方法：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731161225898.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript">
        function changeText(){
            var d = document.getElementById("divMessage");//根据ID获取元素
            d.innerHTML = "才是真的好";//设置元素的内容
        }

        function showSubject(){
            var subjects = document.getElementsByName("subject");//根据name获取元素，返回的是一个集合
            var result = "";
            for(var i=0;i<subjects.length;i++){
                result += subjects[i].innerHTML;
            }
            alert(result);
        }

        function showDiv(){
            var divs = document.getElementsByTagName("div");//根据标签名称获取元素，返回的是一个集合
            var result = "";
            for(var i=0;i<divs.length;i++){
                result += divs[i].innerHTML;
            }
            alert(result);
        }
    </script>
</head>
<body>
    <div id="divMessage">大家好</div>
    <input type="button" value="getElementById" onclick="changeText()" />
    <br>
    <div name="subject">C#</div>
    <div name="subject">java</div>
    <div name="subject">html</div>
    <div name="subject">javascript</div>
    <input type="button" value="getElementsByName" onclick="showSubject()" />
    <input type="button" value="getElementsByTagName" onclick="showDiv()" />
</body>
</html>
```
## visibility和display
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731162239580.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200731162244533.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3N0YXJfb2Zfc2NpZW5jZQ==,size_16,color_FFFFFF,t_70)
visibility和display的区别：元素设置visibility为不可见后该元素还是会占用空间，元素设置display为不可见后该元素不会占用空间。

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
</head>
<body>
    <div id="div1">第一个div</div>
    <div id="div2">第二个div</div>
    <div id="div3">第三个div</div>
    <input type="button" value="使用visibility隐藏第二个div" onclick="document.getElementById('div2').style.visibility='hidden'" />
    <input type="button" value="使用display隐藏第二个div" onclick="document.getElementById('div2').style.display='none'" />
</body>
</html>
```

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <script type="text/javascript">
        function showAndHidden(){
            var d = document.getElementById("myDiv");
            //控制显示和隐藏
            if(d.style.display == "none"){
                d.style.display = "block";
            }else{
                d.style.display = "none";
            }
        }
    </script>
</head>
<body>
    <div id="myDiv">大家晚上好！</div>
    <input type="button" value="显示/隐藏" onclick="showAndHidden()" />
</body>
</html>
```

## history对象
history：用来操作浏览器的历史记录
常用方法如下：
back()：返回上一个页面
forward()：进入下一个页面
go()：到哪个页面去  go(-1)表示上一个页面，相当于back()   
   go(1)表示下一个页面，相当于forward()
   go(-2)表示上上个页面
   
page1.html
```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
</head>
<body>
    这是第一个页面<br>
    <a href="page2.html">进入第二个页面</a>
</body>
</html>
```
page2.html

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
</head>
<body>
    这是第二个页面<br>
    <a href="page3.html">进入第三个页面</a>
    <input type="button" value="进入到历史记录的上个页面" onclick="history.back()" />
    <input type="button" value="进入到历史记录的下个页面" onclick="history.forward()" />
</body>
</html>
```

page3.html

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
</head>
<body>
    这是第三个页面<br>
    <input type="button" value="GO"  onclick="history.go(-2)" >
</body>
</html>
```
## location对象
location：用来操作浏览器的地址
常用属性href：用来设置浏览器的地址  
例如：location.href=”http://www.baidu.com” 浏览器将显示百度网页
常用方法reload()：用于刷新页面

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
</head>
<body>
    <input type="button" value="href" onclick="location.href='http://www.baidu.com'">
    <input type="button" value="reload()" onclick="location.reload()">
</body>
</html>
```

项目代码下载github地址：[https://github.com/MandarinOrange/js_Window_BOM](https://github.com/MandarinOrange/js_Window_BOM)
