## HTML

我在想，要用怎样的方式讲才会让你更高效率的上手。这里就用到了“8/2”法则，用20%的信息产生80%的价值。我就假装我是你，我会：

1. 先了解边界或全貌。就是我们要讲的东西的范围，会给出一系列demo和一个综合的demo，先直观感受一下。
2. 了解逻辑和规则，使用规则。沿着一条主干逻辑讲解技术的来龙去脉，在需要深入或重点理解的地方会稍微深入细节，然后回到主干逻辑继续向下讲，大致效果如下图：

![图片](https://raw.githubusercontent.com/qiuguixin/static/master/%E9%80%BB%E8%BE%91.png)

3. 梳理关键规则，方便查阅。

### 1、一系列demo

早期的HTML主要方便看文档创造的，所以网页也被称作文档，并且JS操作HTML也是对象也是document。这种文档就是用既定的`标记语言`+`超链接`写成的由*文字*和*图片*构成的页面。早期注重图文排版，今天主要增强了布局功能，多了一些音视频、画布的标签，但重点还是图文排版，内容不多，主要就是几个标签和一些布局。

需要掌握的最少必要标签：

图：`img`

文：`p`、`a`

输入：`input`

布局：`div`

列表：`ul`、`li`

其他：`span`

会用这些标签基本上就可以写这个星球上几乎所有的网页，然后其他的标签需要的时候查看文档就行了。

但重点不是写这几个标签，而是怎么用他们写出五花八门的布局效果。

因为内容比较少，下面就只提供一个**[Hello World示例](https://qiuguixin.github.io/fe-demo/html/hello-world.html)**和**[综合示例](https://qiuguixin.github.io/fe-demo/html/simple-demo.html)**来讲。



### 2、来龙去脉

#### Hello World示例

[查看示例](https://qiuguixin.github.io/fe-demo/html/hello-world.html)

欢迎进入HTML世界。所以HTML世界，我来了！

```html
<!DOCTYPE html>
<head>
    <title>Hello World示例</title>
</head>
<body>
    <p>Hello World!</p>
</body>
```

其中，这是HTML的结构：

```html
<html>
    <head>...</head>
    <body>...</body>
</html>
```

继续深入：

1. `<html></html>`为根标签，整个页面都包在它里面。

2. `<head></head> `标签之间可以定义一些页面配置信息，例如页面标题、引用的JS、样式等等。

3. 在`<body></body>`标签之间的内容就是显示给用户看的内容，我们写的所有要显示的网页内容放在这两个标签之间。

继续深入：

1. 上边所说的标签分为**单标签**和**双标签**，注意双标签的**结束标签**标签名前多了个`/`。

2. 双标签之间放内容。

> 哦，对了，`<!DOCTYPE html>`表示我们用的HTML的版本号，浏览器据此来用相应版本的HTML规则来解析我们的HTML代码，了解即可。

至此，我们就可以在页面上显示`Hello World!`了，哈哈😄





#### 综合示例

[查看示例](https://qiuguixin.github.io/fe-demo/html/simple-demo.html)

现在我们已经知道了HTML的一些最基本的知识了，下面给出一个综合示例，展示HTML几个最重要的标签的用法和效果，我们可是要用这几个标签打天下的，可不要小瞧他们哦😁



```html
<!DOCTYPE html>
<head>
    <title>综合示例</title>
</head>
<body>
    <div>
    	<p>这是一段文字:在长大的过程中，我才慢慢发现，我身边的所有事，别人跟我说的所有事，那些所谓本来如此，注定如此的事，它们其实没有非得如此，事情是可以改变的。更重要的是，有些事既然错了，那就该做出改变。</p>

    	<a href="https://www.imooc.com/">点击进入慕课网</a>

    	<img src="https://www.imooc.com/static/img/index/logo.png">

    	<ul>
    		<li>列表项</li>
    		<li>列表项</li>
    		<li>列表项</li>
    		<li>列表项</li>
    		<li>列表项</li>
    	</ul>

    	<input type="text">

    	<p>这是另一段文字:<span>今天很残酷,明天更残酷,后天很美好,但绝对大部分是死在明天晚上。所以每个人不要放弃今天。</span></p>
    </div>
</body>
```

相信大家都用过word文档，使用word文档可以对图文信息进行简单的排版，请注意，在word中我们是使用Word上的工具对我们的内容加工，以达到我们想要的格式。同样的，我们在HTML中要实现想要的图文格式，也需要借助一定的工具，不过这种工具是通过标签实现的，这些标签是已经内置好既定的样式，我们只需要将我们的内容放到相应的标签中即可实现简单的排版。



下面我们就一一介绍下最重要的几个标签。

- `div`: 可以把文档分割为不同的部分，里面可以放各种其他标签。
- `p`: 放文章段落文字。
- `a`: 链接到另一个页面。链接放到它的`href`**属性**里面，标签之间放链接文字，点击文字即可跳转到链接对应的页面。
- `img`: 向页面中插入一张图片。图片链接放到它的`src`**属性**里面，注意这是个单标签。
- `ul`和`li`: 用来定义一个列表，就像你在word上的一条一条的文字一样。其中ul是列表的容器，li标签之间放列表的内容。
- `input`: 文字输入框，可以输入文字。

需要说明的是，

1. **属性**，就像一个人有身高、体重、性别等这些都是描述一个人的特征的，HTML标签也有属性，有些有内定的特殊的作用，有些是存储元素功能多信息的。

   属性的写法：

   - 属性总是以名称/值对的形式出现，比如：*name="value"*。
   - 属性总是在 HTML 元素的*开始标签*中规定。

   - HTML标签都有title属性，鼠标放标签上面会把该属性内容显示出来
   - HTML标签还有id、class、style等具有特殊作用的属性，还可以自定义属性，后面会讲。

2. **代码注释**，代码注释的作用是帮助程序员标注代码的用途，不会影响页面的显示和布局。语法就是`<!--****注释文字 -->`
3. 还有其他90%的标签，忘掉他们，至少现在不需要了解。







## CSS

### 从哪里来？

HTML只能完成一些基本的图文排版，但要实现更丰富多彩的网页界面，还需要对布局进行更详细的控制，于是就产生了CSS。

那为什么不直接用HTML语言来控制呢？主要是还是太复杂了嘛，而且结构和样式混为一谈，也不好维护，所以就再出一个语言，分而治之。

出一门新的语言就会引出一堆新的概念，为什么会有这些概念，这些概念是基于什么的考量出来的，只有很深入理解这门新的语言才能理解，所以，我们现在只要弄清楚概念就行。

CSS全称为“层叠样式表 (Cascading Style Sheets)”，为什么叫**层叠**样式表？后面再讲吧。

整体而言，只要掌握如下几点就可以完成80%的页面布局：

1. 样式在哪里写？[查看示例](https://qiuguixin.github.io/fe-demo/html/style-where-to-write.html)
2. 样式怎么找到对应HTML元素并对它起作用？
3. CSS最核心的知识是什么——盒模型
4. 定位和居中
5. 最简单的写法——flex布局



### 样式在哪里写？

从内CSS样式写在哪来考虑的话，样式分**内联式**、**嵌入式**和**外部式**三种。

- **内敛式**：就是把css代码直接写在现有的HTML开始标签中，如下面代码：

```
<p style="color:red">这里文字是红色。</p>
```

> css样式代码要写在`style=""`双引号中，如果有多条css样式代码设置可以写在一起，中间用分号`;`隔开。如下代码：

```
<p style="color:red;font-size:12px">这里文字是红色。</p>
```



> 使用内联样式已经可以给元素设置我们想要的样式了，但是若要批量设置样式，那么每个元素都要重复的写同样的样式代码，不仅费时费力而且也没有样式跟结构的分离，CSS也没有存在的价值了。因此出现了**嵌入式**样式。

- **嵌入式**：样式可以脱离HTML元素，写在`<style></style>`标签里，从而对选中的HTML标签都起作用，如：

```html
<!DOCTYPE HTML>
<html>
<head>
    <style>
        p{
            color:red;
        }
    </style>
</head>
<body>
    <p>慕课网，专注服务互联网工程师快速成为技术高手！</p>
    <p>慕课网，专注服务互联网工程师快速成为技术高手！</p>
    <p>慕课网，专注服务互联网工程师快速成为技术高手！</p>
</body>
</html>
```

> 这样所有的`<p></p>`都有上面的样式



> 再一次，如果HTML中有太多样式怎么办？我们可不可以把样式放到别的文件里？答案是可以的。

- **外部式**: 把css代码写一个单独的外部文件中，这个css样式文件以“`.css`”为扩展名，在<head>内使用<link>标签将css样式文件链接到HTML文件内,  如：

```
<!DOCTYPE HTML>
<html>
<head>
	<link href="style.css" rel="stylesheet" type="text/css" />
</head>
<body>
    <p>慕课网，专注服务互联网工程师快速成为技术高手！</p>
    <p>慕课网，专注服务互联网工程师快速成为技术高手！</p>
</body>
</html>
```

`style.css`内容:

```css
p{
    color:red;
}
```



有以下注意点：

1. <link>和<style>标签位置一般写在<head>标签之内。
2. 如果有一种情况：对于同一个元素我们同时用了三种方法设置css样式，那么哪种方法真正有效呢？

答案：内联式>(嵌入式 和 外部式后面的覆盖前面的)，具体下节讲。



### 样式怎么找到对应HTML元素并对它起作用？

这就涉及到一个新的概念：**CSS选择器**。

CSS选择器就是通过匹配HTML的特性和HTML标签之间的关系，来找到对应HTML标签，然后对其添加样式的。

选择器总共有60种左右，我们重点掌握七八种即可，其他需要的时候看文档即可，本节比较重要。

我们要讲的选择器如下：

- 标签选择器
- 类选择器
- ID选择器
- 子选择器、后代选择器、分组选择器
- 伪类选择器
- 通用选择器

另：样式的继承和优先级



#### **标签选择器**

> 其实就是HTML标签名如: html、body、p、img。

如下代码：

```
p{
    color:red;
}
```
> 这样就对所有p标签设置了对应样式



#### **类选择器**

> 通过给HTML标签添加一个`class`属性，然后根据该属性值来设置样式。HTML会根据匹配到所有class=该属性值的元素，并对其设置对应样式。

语法：

```
.类选器名称{css样式代码;}
```

使用方法：

1. 使用class="类选择器名称"为标签设置一个类，如下：

```
<span class="stress">胆小如鼠</span>
```

2. 设置类选器css样式，如下：

```
.stress{color:red;}
```



**注意**：我们还可以给class设置多个值，每个值都可以设置样式，然后所有class值对应的样式都会对元素起作用

例如：

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        .list-item{
            color: black;
        }
        .active{
            font-size: 16px;
        }
    </style>
</head>
<body>
    <ul>
        <li class="list-item active">列表项</li>
        <li class="list-item ">列表项</li>
        <li class="list-item ">列表项</li>
        <li class="list-item ">列表项</li>
        <li class="list-item ">列表项</li>
    </ul>
</body>
</html>
```

> 所有class="list-item"的元素字体颜色都是black的，第一个除了是字体颜色是black，字体大小还是16px,因为它的class中包含active。



#### **ID选择器**

> 通过给HTML标签添加一个`id`属性，然后根据该属性值来设置样式。HTML会根据匹配到所有id=该属性值的元素，并对其设置对应样式。

**注意**：与**类选择器**不同的是**ID选择器**有以下特点：

1. 对应HTML标签的`id`属性
2. HTML标签的`id`属性只能包含一个值，并且全局唯一
3. ID选择符的前面是井号**（#）**号，而不是英文圆点**（.）**

例如：

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        #item1{
            font-size: 16px;
        }
    </style>
</head>
<body>
    <ul>
        <li class="list-item" id="item1">列表项</li>
        <li class="list-item ">列表项</li>
    </ul>
</body>
</html>
```





#### 子选择器、后代选择器、分组选择器

- 子选择器，即大于符号(>),用于选择指定标签元素的**第一代子元素**。

例如：

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        li>div{
            border: 2px solid red;
            width: 100px;
            height: 100px;
            padding: 20px;
        }
        /* li>div>div{
            border: 2px solid red;
            width: 100px;
            height: 100px;
            padding: 20px;
        } */
    </style>
</head>
<body>
    <ul>
        <li>
        	<div>
                第一代子元素
                <div>第二代子元素</div>
        	</div>
        </li>
        <li>
            <span>第一代子元素
                <div>第二代子元素</div>
            </span>    
        </li>
    </ul>
</body>
</html>
```



- 包含选择器，即加入空格,用于选择指定标签元素下的**后辈元素**。

> 与子选择器的区别是：**>**作用于元素的第一代后代，**空格**作用于元素的所有后代。

例如：

```html
<!DOCTYPE html>
<html>
<head>
    <style>
        li div{
            border: 2px solid red;
            width: 100px;
            height: 100px;
            padding: 20px;
        }
        
    </style>
</head>
<body>
    <ul>
        <li>
        	<div>
                第一代子元素
                <div>第二代子元素</div>
        	</div>
        </li>
        <li>
            <span>第一代子元素
                <div>第二代子元素</div>
            </span>    
        </li>
    </ul>
</body>
</html>
```



- 分组选择器，即逗号（，）,它的作用是为**多个选择器**设置同一个样式

例如：

如下代码为h1、span标签同时设置字体颜色为红色：

```
h1,span{color:red;}
```

它相当于下面两行代码：

```
h1{color:red;}
span{color:red;}
```



#### 伪类选择器

> 它允许给html不存在的标签（标签的某种状态）设置样式

例如事先给a标签设置鼠标滑过的样式，当鼠标悬停的时候就会显示该样式

例如：

```
a:hover{color:red;}
```

上面一行代码就是为 a 标签鼠标滑过的状态设置字体颜色变红。





#### 通用选择器

> 它使用一个（*）号指定，它的作用是匹配html中所有标签元素, 通常用于项目开始给元素统一设置某种样式或者是覆盖元素默认的样式

例如：

任意标签元素字体颜色全部设置为红色：

```
* {color:red;}
```

> 上面代码就给任意标签元素字体颜色全部设置为红色



#### 样式的继承和优先级

- 样式继承

CSS的**某些样式**是具有继承性的，那么什么是继承呢？继承是一种规则，它允许样式不仅应用于某个特定html标签元素，而且应用于其后代。

比如下面代码：如某种颜色应用于p标签，这个颜色设置不仅应用p标签，还应用于p标签中的所有子元素文本，这里子元素为span标签。

```
p{color:red;}

<p>三年级时，我还是一个<span>胆小如鼠</span>的小女孩。</p>
```

注意：具有继承性的样式主要就是文字的样式。[详见](https://www.cnblogs.com/thislbq/p/5882105.html)



- 优先级

> CSS 选择器有很多，不同的选择器的权重和优先级不一样，对于一个元素，如果存在多个选择器，那么就需要根据权重来计算其优先级。

权重分为四级，分别是：

1. 代表内联样式，如style="xxx"，权值为 1000；
2. 代表 ID 选择器，如#content，权值为 100；
3. 代表类、伪类和属性选择器，如.content、:hover、[attribute]，权值为 10；
4. 代表元素选择器和伪元素选择器，如div、p，权值为 1。

需要注意的是：通用选择器（*）、子选择器（>）和相邻同胞选择器（+）并不在这四个等级中，所以他们的权值都为 0。 权重值大的选择器其优先级也高，相同权重的优先级又遵循**后定义覆盖前面定义**的情况。

```
p{color:red;} /*权值为1*/
p span{color:green;} /*权值为1+1=2*/
.warning{color:white;} /*权值为10*/
p span.warning{color:purple;} /*权值为1+1+10=12*/
#footer .note p{color:yellow;} /*权值为100+10+1=111*/
```



那么问题来了，我要给某个样式设置最高权限怎么办？用**!important**来解决。

如下代码：

```
p{color:red!important;}
p{color:green;}
<p class="first">三年级时，我还是一个<span>胆小如鼠</span>的小女孩。</p>

```

这时 p 段落中的文本会显示的red红色。

**注意：!important要写在分号的前面**



所以完整的单个选择器优先级比较：

css属性!important

　　`>` 内联样式 

　　`>` ID选择器(#id)

　　`>` 类选择器(.class) = 伪类选择器(:hover等) = 属性选择器[type等] 

　　`>` 元素选择器(p等) = 伪元素选择器(:after/:before/::selection等) 

　　`>` 通用选择器(*) 

> 注：没提到的属性选择器、伪类选择器自行学习





### CSS最核心的知识是什么——盒模型

> 前面全是铺垫！全是铺垫！到这里才真正开始讲样式如何写。

那我们要理解如下问题：

1. 什么是盒模型？
2. 怎么用盒模型来布局？



#### 什么是盒模型？

> 就像我们收到的快递，本来买了一部小小的手机，收到的却是那么大一个盒子。因为手机白色的包装盒和手机机器之间有间隔层（内边距: padding），手机白色盒子有厚度，虽然很薄（边框: border），盒子和快递箱子之间还有一层泡沫板（外边距: margin）。这就是一个典型的盒子。 

CSS主要就是基于该模型来布局的。



#### 怎么用盒模型来布局？

因为每个元素其实就是个盒子，我们都是通过设置元素的宽高、内边距、边框、外边距来控制元素的占位。

具体的：

##### 设置宽高（width\height）

但是这里需要了解一下，元素的分类：

- 有些元素默认占一行，可以设置宽高，这种叫**块级元素**（block）,比如`<div>`、` <p>`、`<h1>`、`<ul>` 和 `<li>`
- 有些元素默认占内容大小，不可以设置宽高，这种叫**内联元素**（inline），比如`<span>`、`<a>`
- 有些元素默认占内容大小，可以设置宽高，这种叫**内联块元素**（inline-block），比如`<img>`、`<input>`

> 对于不可设置宽高的内联元素我们需要先把他转成块状元素，才可以设置固定的宽高

```css
span{
    display: inline-block;
    width: 100px;
	height: 100px; 
}

```

如上就给span元素设置了宽高各100px.

##### 设置内边距(padding)

内边距也叫填充。

填充也可分为上、右、下、左(顺时针)。如下代码：

```
div{padding:20px 10px 15px 30px;}
```

顺序一定不要搞混。可以分开写上面代码：

```
div{
   padding-top:20px;
   padding-right:10px;
   padding-bottom:15px;
   padding-left:30px;
}
```

如果上、右、下、左的填充都为10px;可以这么写

```
div{padding:10px;}
```

如果上下填充一样为10px，左右一样为20px，可以这么写：

```
div{padding:10px 20px;}
```



##### 设置边框(border)

盒子模型的边框就是围绕着内容及填充的线，这条线你可以设置它的粗细、样式和颜色(边框三个属性)。

如下面代码为 div 来设置边框粗细为 2px、样式为实心的、颜色为红色的边框：

```
div{
    border:2px  solid  red;
}

```

上面是 border 代码的缩写形式，可以分开写：

```
div{
    border-width:2px;
    border-style:solid;
    border-color:red;
}

```

**注意：**

1、border-style（边框样式）常见样式有：

dashed（虚线）| dotted（点线）| solid（实线）。

2、border-color（边框颜色）中的颜色可设置为十六进制颜色，如:

```
border-color:#888;//颜色是十六进制写法，还可以rgb形式，比如rgb(0,0,0)
```

3、border-width（边框宽度）单位像素（px）。



现在有一个问题，如果有想为 div 标签单独设置下边框，而其它三边都不设置边框样式怎么办呢？css 样式中允许只为一个方向的边框设置样式：

```
div{border-bottom:1px solid red;}
```

同样可以使用下面代码实现其它三边(上、右、左)边框的设置：

```
div{
    border-top:1px solid red;
    border-right:1px solid red; 
    border-left:1px solid red;
}
```



##### 设置外边距(margin)

> 设置外边距跟设置内边距类似，只是作用的位置不同。

外边框也是可分为上、右、下、左。如下代码：

```
div{margin:20px 10px 15px 30px;}
```

也可以分开写：

```
div{
   margin-top:20px;
   margin-right:10px;
   margin-bottom:15px;
   margin-left:30px;
}
```

如果上右下左的外边框都为10px;可以这么写：

```
div{ margin:10px;}
```

如果上下外边框一样为10px，左右一样为20px，可以这么写：

```
div{ margin:10px 20px;}
```

> **注意**：这里提到 margin，就不得不提一下 margin 的这一特性——纵向重叠。如<p>的纵向 margin 是 16px，那么两个<p>之间纵向的距离是多少？—— 按常理来说应该是 16 + 16 = 32px，但是答案仍然是 16px。因为纵向的 margin 是会重叠的，如果两者不一样大的话，大的会把小的“吃掉”。



##### 元素的实际占位大小

盒模型宽度和高度和我们平常所说的物体的宽度和高度理解是不一样的，css内定义的宽（width）和高（height），指的是填充以里的内容范围。

因此一个元素实际宽度（盒子的宽度）=左边界+左边框+左填充+内容宽度+右填充+右边框+右边界。

比如：

css代码：

```
div{
    width:200px;
    padding:20px;
    border:1px solid red;
    margin:10px;    
}

```

html代码：

```
<body>
   <div>文本内容</div>
</body>
```

元素的实际长度为：10px+1px+20px+200px+20px+1px+10px=262px。在chrome浏览器下可查看元素盒模型，如下图：

[![img](http://img.mukewang.com/543b4cae0001b34304300350.jpg)](http://img.mukewang.com/543b4cae0001b34304300350.jpg)



前面提到，为盒子模型占位大小还要通过计算得到而不是实际设置的width\height。

如何解决这一问题？答案就是为盒子指定样式：box-sizing:border-box。

**这个知识点很重要！！！**

这样设置的宽高就是元素的占位的宽高（不算margin），padding\border都往内部挤。

比如：

```css
div{
    box-sizing:border-box;
    width:200px;
    padding:20px;
    border:1px solid red;
    margin:10px;    
}
```



那么div的实际占位宽度就＝外边距+宽=10px+200px

这个在手机端最常用，当要设置内容宽度为屏幕宽度的100%时，只用设置元素(比如div)：

```css
div{
   box-sizing:border-box;
   width: 100%;
}
```



建议在为系统写 CSS 时候，第一个样式就是： 

```
* {
	box-sizing:border-box;
}
```





### 定位和浮动

> 定位和浮动布局是CSS中比较特殊和比较常用的布局形式，我们摘出来讲一下。

是时候了解一下CSS包含3种基本的布局模型了：

1、流动模型（Flow）：正常的从上到下、从左到右布局，是默认的网页布局模式
2、浮动模型 (Float)：脱离flow，使元素可以左右浮动
3、层模型（Layer）：就像图像软件Ps中的图层一样可以对每个图层能够精确定位操作

##### 定位

如何让html元素在网页中精确定位？就像图像软件PhotoShop中的图层一样可以对每个图层能够精确定位操作？CSS定义了一组定位（positioning）属性来支持层布局模型。

层模型有三种形式：

1、**绝对定位**(position: absolute)

2、**相对定位**(position: relative)

3、**固定定位**(position: fixed)



1. 绝对定位

如果想为元素设置层模型中的绝对定位，需要设置**position:absolute**(表示绝对定位)，这条语句的作用将元素从文档流中拖出来，然后使用left、right、top、bottom属性相对于其最接近的一个具有定位属性的父包含块进行绝对定位。如果不存在这样的包含块，则相对于body元素，即相对于**浏览器窗口**。

如下面代码可以实现div元素相对于浏览器窗口向右移动100px，向下移动50px。

```
div{
    width:200px;
    height:200px;
    border:2px red solid;
    position:absolute;
    left:100px;
    top:50px;
}
<div id="div1"></div>
```

效果如下：

![img](http://img.mukewang.com/53a00b130001e86707360547.jpg)



使用`position:absolute`可以实现被设置元素相对于浏览器（body）设置定位以后，大家有没有想过可不可以相对于其它元素进行定位呢？答案是肯定的，当然可以。使用position:relative来帮忙，但是必须遵守下面规范：

1、参照定位的元素必须是相对定位元素的前辈元素：

```
<div id="box1"><!--参照定位的元素-->
    <div id="box2">相对参照元素进行定位</div><!--相对定位元素-->
</div>


```

从上面代码可以看出box1是box2的父元素（父元素当然也是前辈元素了）。

2、参照定位的元素必须加入position:relative;

```
#box1{
    width:200px;
    height:200px;
    position:relative;        
}


```

3、定位元素加入position:absolute，便可以使用top、bottom、left、right来进行偏移定位了。

```
#box2{
    position:absolute;
    top:20px;
    left:30px;         
}


```

这样box2就可以相对于父元素box1定位了（这里注意参照物就可以不是浏览器了，而可以自由设置了）。



2. 相对定位

如果想为元素设置层模型中的相对定位，需要设置position:relative（表示相对定位），它通过left、right、top、bottom属性确定元素在**正常文档流中**的偏移位置。相对定位完成的过程是首先按static(float)方式生成一个元素(并且元素像层一样浮动了起来)，然后相对于**以前的位置移动，**移动的方向和幅度由left、right、top、bottom属性确定，偏移前的位置保留不动。

如下代码实现相对于以前位置向下移动50px，向右移动100px;

```
#div1{
    width:200px;
    height:200px;
    border:2px red solid;
    position:relative;
    left:100px;
    top:50px;
}

<div id="div1"></div>

```

效果图：

![img](http://img.mukewang.com/53a00d2b00015c4b06190509.jpg)

什么叫做“偏移前的位置保留不动”呢？

大家可以做一个实验，在右侧代码编辑器的19行div标签的后面加入一个span标签，在标并在span标签中写入一些文字。如下代码：

```
<body>
    <div id="div1"></div><span>偏移前的位置还保留不动，覆盖不了前面的div没有偏移前的位置</span>
</body>

```

效果图：

[![img](http://img.mukewang.com/541a4bfc0001abef05940489.jpg)](http://img.mukewang.com/541a4bfc0001abef05940489.jpg)

从效果图中可以明显的看出，虽然div元素相对于以前的位置产生了偏移，但是div元素以前的位置还是保留着，所以后面的span元素是显示在了div元素以前位置的后面。



3. 固定定位

fixed：表示固定定位，与absolute定位类型类似，但它的相对移动的坐标是视图（**屏幕内的网页窗口**）本身。由于视图本身是固定的，它不会随浏览器窗口的滚动条滚动而变化，除非你在屏幕中移动浏览器窗口的屏幕位置，或改变浏览器窗口的显示大小，因此固定定位的元素会始终位于浏览器窗口内视图的某个位置，不会受文档流动影响，这与background-attachment:fixed;属性功能相同。以下代码可以实现相对于**浏览器视图**向右移动100px，向下移动50px。并且拖动滚动条时位置固定不变。

```
#div1{
    width:200px;
    height:200px;
    border:2px red solid;
    position:fixed;
    left:100px;
    top:50px;
}
<div id="div1"></div>
<p>文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本。</p>
....

```



##### 浮动

块状元素这么霸道都是独占一行，如果现在我们想让两个块状元素并排显示，怎么办呢？不要着急，设置元素浮动就可以实现这一愿望。

如下代码可以实现两个 div 元素一行显示。

```
div{
    width:200px;
    height:200px;
    border:2px red solid;
    float:left;
}
<div id="div1"></div>
<div id="div2"></div>

```

效果图

[![img](http://img.mukewang.com/540e62c60001c56a06760417.jpg)](http://img.mukewang.com/540e62c60001c56a06760417.jpg)

当然你也可以同时设置两个元素右浮动也可以实现一行显示。

```
div{
    width:200px;
    height:200px;
    border:2px red solid;
    float:right;
}

```

效果图

[![img](http://img.mukewang.com/540e632b0001f5f506760417.jpg)](http://img.mukewang.com/540e632b0001f5f506760417.jpg)

又有小伙伴问了，设置两个元素一左一右可以实现一行显示吗？当然可以：

```
div{
    width:200px;
    height:200px;
    border:2px red solid;
}
#div1{float:left;}
#div2{float:right;}

```

效果图

[![img](http://img.mukewang.com/540e63b50001f6a206760417.jpg)](http://img.mukewang.com/540e63b50001f6a206760417.jpg)

 

**注意**：子元素设置为浮动会造成父元素塌陷，因为子元素浮动之后不占flow位置了，父元素就扁了。

这时可以通过设置父元素样式为`overflow: hidden`来清除浮动对父元素布局的影响。





### 最简单的写法——flex布局

> 布局的传统解决方案基于盒子模型，依赖 display 属性 + position 属性 + float 属性。它对于那些特殊布局非常不方便，比如，垂直居中（下文会专门讲解）就不容易实现。在目前主流的移动端页面中，使用 flex 布局能更好地完成需求，因此 flex 布局的知识是必须要掌握的。

我们先上几个例子来了解一下flex的简洁。

[元素在父盒子内水平垂直居中](https://qiuguixin.github.io/fe-demo/html/style-flex-1.html)

[固定-自适应布局](https://qiuguixin.github.io/fe-demo/html/style-flex-2.html)

#### 元素在父盒子内水平垂直居中

![](http://pj4frwcfh.bkt.clouddn.com/18-12-14/11129071.jpg)

```html
<!DOCTYPE html>
<head>
    <title>flex布局</title>
    <style>
        .container{
            width: 800px;
            margin: 0 auto;
        }
        .box{
            border: 1px solid red;
        }
        .box-1{
            height: 100px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .box-1 .flex-item{
            border: 1px solid blue;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="box box-1">
            <div class="flex-item">我水平垂直居中</div>
        </div>
    </div>
</body>
```

注意上面这三行代码：

```css
display: flex;
justify-content: center;
align-items: center;
```

用flex布局，只用在父元素上设置这三行代码就可以实现子元素在父元素内水平垂直居中。

- `display: flex;`指定为 Flex 布局
- `justify-content: center;`主轴方向上居中
- `align-items: center;`主轴垂直方向上居中



#### 固定-自适应布局

![](http://pj4frwcfh.bkt.clouddn.com/18-12-14/62250112.jpg)

```html
<!DOCTYPE html>
<head>
    <title>flex布局</title>
    <style>
        .container{
            width: 800px;
            margin: 0 auto;
        }
        .box{
            border: 1px solid red;
        }
    </style>
    <style>
        .box-2{
            height: 100px;
            display: flex;
        }
        .box-2 .flex-item-1{
            border: 1px solid blue;
            width: 100px;
        }
        .box-2 .flex-item-2{
            border: 1px solid blue;
            flex: 1;
        }
    </style>
</head>
<body>
    <div class="container">
        <p>固定-自适应布局：</p>
        <div class="box box-2">
            <div class="flex-item-1">我固定</div>
            <div class="flex-item-2">我自适应</div>
        </div>
    </div>
</body>
```

- 固定宽度的元素设置固定宽度
- 自适应的元素占用剩余空间设置`flex: 1;`

#### 语法

外面父元素设置`display: flex`后，会有如下可设置属性：

```
flex-direction
flex-wrap
justify-content
align-items
align-conte
```

##### flex-direction

[查看示例]()

![](http://pj4frwcfh.bkt.clouddn.com/18-12-14/37012903.jpg)

决定主轴的方向。有四个值：

- `row`（默认值）：主轴为水平方向，起点在左端。
- `row-reverse`：主轴为水平方向，起点在右端。
- `column`：主轴为垂直方向，起点在上沿。
- `column-reverse`：主轴为垂直方向，起点在下沿。

```css
.box {
  flex-direction: row | row-reverse | column | column-reverse;
}
```

##### flex-wrap

![](http://pj4frwcfh.bkt.clouddn.com/18-12-14/33730417.jpg)

决定项目在主轴上换不换行、如何换行。有三个值：

- `nowrap`（默认）：不换行。
- `wrap`：换行，第一行在上方。
- `wrap-reverse`：换行，第一行在下方。

```
.box{
  flex-wrap: nowrap | wrap | wrap-reverse;
}
```



##### justify-content

![](http://pj4frwcfh.bkt.clouddn.com/18-12-14/24079314.jpg)

决定项目在主轴上的对齐方式。有5个值：

- `flex-start`（默认值）：左对齐
- `flex-end`：右对齐
- `center`： 居中
- `space-between`：两端对齐，项目之间的间隔都相等。
- `space-around`：每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。

```
.box {
  justify-content: flex-start | flex-end | center | space-between | space-around;
}
```



##### align-items

![](http://pj4frwcfh.bkt.clouddn.com/18-12-14/9389087.jpg)

决定项目在主轴垂直方向上如何对齐。同样有5个值：

- `flex-start`：交叉轴的起点对齐。
- `flex-end`：交叉轴的终点对齐。
- `center`：交叉轴的中点对齐。
- `baseline`: 项目的第一行文字的基线对齐。
- `stretch`（默认值）：如果项目未设置高度或设为auto，将占满整个容器的高度。

```
.box {
  align-items: flex-start | flex-end | center | baseline | stretch;
}
```







##### align-content

![](http://pj4frwcfh.bkt.clouddn.com/18-12-14/3345015.jpg)

决定**多行**项目在主轴垂直方向上如何对齐（单行不起作用）。同样有5个值：

- `flex-start`：交叉轴的起点对齐。
- `flex-end`：交叉轴的终点对齐。
- `center`：交叉轴的中点对齐。
- `baseline`: 项目的第一行文字的基线对齐。
- `stretch`（默认值）：如果项目未设置高度或设为auto，将占满整个容器的高度。

```
.box {
  align-items: flex-start | flex-end | center | baseline | stretch;
}
```



项目的属性有6个：

```
order
flex-grow
flex-shrink
flex-basis
flex
align-self
```

这里直讲两个最常用的：`flex`和`align-self`,剩下的忽略。

##### flex

两种常见情况：

- 当只给一个项目设置`flex: 1;`，则该项目占据父元素剩余的空间

- 当给所有项目设置`flex: 1;`，则项目平局分布父元素空间

![](http://pj4frwcfh.bkt.clouddn.com/18-12-14/42147884.jpg)

```
<div class="Grid">
  <div class="Grid-cell">...</div>
  <div class="Grid-cell">...</div>
  <div class="Grid-cell">...</div>
</div>
```

```
.Grid {
  display: flex;
}

.Grid-cell {
  flex: 1;
}
```

其他参考[阮一峰的教程](http://www.ruanyifeng.com/blog/2015/07/flex-examples.html)

##### align-self

![](http://pj4frwcfh.bkt.clouddn.com/18-12-14/88232316.jpg)

允许单个项目设置与其他项目在**垂直主轴方向**有不一样的对齐方式，可覆盖`align-items`属性，有6个值，默认值auto表示继承父元素的`align-items`属性。

```css
.item {
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}
```









### 其他补充



#### 文字排版--字体

我们可以使用css样式为网页中的文字设置字体、字号、颜色等样式属性。下面我们来看一个例子，下面代码实现：为网页中的文字设置字体为宋体。

```
body{font-family:"宋体";}
```

这里注意不要设置不常用的字体，因为如果用户本地电脑上如果没有安装你设置的字体，就会显示浏览器默认的字体。（因为用户是否可以看到你设置的字体样式取决于用户本地电脑上是否安装你设置的字体。）
现在一般网页喜欢设置“微软雅黑”，如下代码：

```
body{font-family:"Microsoft Yahei";}
```

或

```
body{font-family:"微软雅黑";}
```

注意：第一种方法比第二种方法兼容性更好一些。

因为这种字体即美观又可以在客户端安全的显示出来（用户本地一般都是默认安装的）。



#### 文字排版--字号、颜色

可以使用下面代码设置网页中文字的字号为12像素，并把字体颜色设置为#666(灰色)：

```
body{font-size:12px;color:#666}
```



#### 文字排版--粗体

我们还可以使用css样式来改变文字的样式：粗体、斜体、下划线、删除线，可以使用下面代码实现设置文字以粗体样式显示出来。

```
p span{font-weight:bold;}
```

在这里大家可以看到，如果想为文字设置粗体是有单独的css样式来实现的，再不用为了实现粗体样式而使用h1-h6或strong标签了。



#### 文字排版--斜体

以下代码可以实现文字以斜体样式在浏览器中显示：

```
p a{font-style:italic;}

<p>三年级时，我还是一个<a>胆小如鼠</a>的小女孩。</p>
```



#### 文字排版--下划线

有些情况下想为文字设置为下划线样式，这样可以在视觉上强调文字，可以使用下面代码来实现：

```
p a{text-decoration:underline;}

<p>三年级时，我还是一个<a>胆小如鼠</a>的小女孩。</p>
```



#### 文字排版--删除线

如果想在网页上设置删除线怎么办，这个样式在电商网站上常会见到：

![img](http://img.mukewang.com/53a0149700010f4802370316.jpg)

上图中的原价上的删除线使用下面代码就可以实现：

```
 .oldPrice{text-decoration:line-through;}
```



#### 段落排版--缩进

中文文字中的段前习惯空两个文字的空白，这个特殊的样式可以用下面代码来实现：

```
p{text-indent:2em;}
<p>1922年的春天，一个想要成名名叫尼克卡拉威（托比?马奎尔Tobey Maguire 饰）的作家，离开了美国中西部，来到了纽约。那是一个道德感渐失，爵士乐流行，走私为王，股票飞涨的时代。为了追寻他的美国梦，他搬入纽约附近一海湾居住。</p>
```


注意：2em的意思就是文字的2倍大小。



#### 段落排版--行间距（行高）

这一小节我们来学习一下另一个在段落排版中起重要作用的行间距（行高）属性（line-height），如下代码实现设置段落行间距为1.5倍。

```
p{line-height:1.5em;}
<p>菲茨杰拉德，二十世纪美国文学巨擘之一，兼具作家和编剧双重身份。他以诗人的敏感和戏剧家的想象为"爵士乐时代"吟唱华丽挽歌，其诗人和梦想家的气质亦为那个奢靡年代的不二注解。</p>
```



#### 段落排版--中文字间距、字母间距

**中文字间隔、字母间隔设置：**

如果想在网页排版中设置**文字间隔**或者**字母间隔**就可以使用    **letter-spacing** 来实现，如下面代码：

```
h1{
    letter-spacing:50px;
}
...
<h1>了不起的盖茨比</h1>
```

注意：这个样式使用在英文单词时，是设置字母与字母之间的间距。

**单词间距设置**：

如果我想设置英文单词之间的间距呢？可以使用 **word-spacing** 来实现。如下代码：

```
h1{
    word-spacing:50px;
}
...
<h1>welcome to imooc!</h1>
```



#### 段落排版--对齐

想为**块状元素**中的文本、图片设置居中样式吗？可以使用text-align样式代码，如下代码可实现文本居中显示。(那么什么是块状元素呢？在后面的11-1、11-2小节中会讲到。)

```
h1{
    text-align:center;
}
<h1>了不起的盖茨比</h1>
```

同样可以设置居左：

```
h1{
    text-align:left;
}
<h1>了不起的盖茨比</h1>
```

还可以设置居右：

```
h1{
    text-align:right;
}
<h1>了不起的盖茨比</h1>
```





#### 盒模型代码简写

还记得在讲盒模型时外边距(margin)、内边距(padding)和边框(border)设置上下左右四个方向的边距是按照顺时针方向设置的：上右下左。具体应用在margin和padding的例子如下：

```
margin:10px 15px 12px 14px;/*上设置为10px、右设置为15px、下设置为12px、左设置为14px*/
```

通常有下面三种缩写方法:

1、如果top、right、bottom、left的值相同，如下面代码：

```
margin:10px 10px 10px 10px;
```

可缩写为：

```
margin:10px;
```

2、如果top和bottom值相同、left和 right的值相同，如下面代码：

```
margin:10px 20px 10px 20px;
```

可缩写为：

```
margin:10px 20px;
```

3、如果left和right的值相同，如下面代码：

```
margin:10px 20px 30px 20px;
```

可缩写为：

```
margin:10px 20px 30px;
```

注意：padding、border的缩写方法和margin是一致的。



#### 颜色值缩写

关于颜色的css样式也是可以缩写的，当你设置的颜色是16进制的色彩值时，如果每两位的值相同，可以缩写一半。

例子1：

```
p{color:#000000;}
```

可以缩写为：

```
p{color: #000;}
```

例子2：

```
p{color: #336699;}
```

可以缩写为：

```
p{color: #369;}
```





#### 颜色值

在网页中的颜色设置是非常重要，有字体颜色（color）、背景颜色（background-color）、边框颜色（border）等，设置颜色的方法也有很多种：

1、英文命令颜色

前面几个小节中经常用到的就是这种设置方法：

```
p{color:red;}
```

2、RGB颜色

这个与 photoshop 中的 RGB 颜色是一致的，由 R(red)、G(green)、B(blue) 三种颜色的比例来配色。

```
p{color:rgb(133,45,200);}
```

每一项的值可以是 0~255 之间的整数，也可以是 0%~100% 的百分数。如：

```
p{color:rgb(20%,33%,25%);}
```

3、十六进制颜色

这种颜色设置方法是现在比较普遍使用的方法，其原理其实也是 RGB 设置，但是其每一项的值由 0-255 变成了十六进制 00-ff。

```
p{color:#00ffff;}
```

配色表：

[![img](http://img.mukewang.com/54c5b4120001f20808000902.jpg)](http://img.mukewang.com/54c5b4120001f20808000902.jpg)

（单击图片可放大）



#### 长度值

长度单位总结一下，目前比较常用到px（像素）、em、% 百分比，要注意其实这三种单位都是相对单位。

**1、像素**

像素为什么是相对单位呢？因为像素指的是显示器上的小点（CSS规范中假设“90像素=1英寸”）。实际情况是会和显示器的实际像素值有关，在目前大多数的设计者都倾向于使用像素（px）作为单位。

**2、em**

就是**本元素**给定字体的 font-size 值，如果元素的 font-size 为 14px ，那么 1em = 14px；如果 font-size 为 18px，那么 1em = 18px。如下代码：

```
p{font-size:12px;text-indent:2em;}
```

上面代码就是可以实现段落首行缩进 24px（也就是两个字体大小的距离）。

**下面注意一个特殊情况：**

但当给 font-size 设置单位为 em 时，此时计算的标准以 p 的父元素的 font-size 为基础。如下代码：

html:

```
<p>以这个<span>例子</span>为例。</p>
```

css:

```
p{font-size:14px}
span{font-size:0.8em;}
```

结果 span 中的字体“例子”字体大小就为 11.2px（14 * 0.8 = 11.2px）。

**3、百分比**

```
p{font-size:12px;line-height:130%}
```

设置行高（行间距）为字体的130%（12 * 1.3 = 15.6px）。



