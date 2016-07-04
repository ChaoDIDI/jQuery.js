# jQuery 入门

**开始前我们先了解一下jQuery请参照下面链接jQuery官网** 
 
 
 
 [jQuery](http://http://jquery.com/)请点击jQuery样式进入到链接地址
 
 [jQuery下载地址](http://www.bootcdn.cn/jquery/)让我们选择复制链接.导入到自己的html中
 <script src="//cdn.bootcss.com/jquery/3.0.0/core.js"></script>
 
 
      这里先阐述下jQuery .它的应用是在你电脑已经安装过node.js的前提下使用.它不是一个插件.有它的存在我们在代码中,实现自己想要的效果,让我们的代码海添加一份绿一份红.
 **接下来我将演示一遍我们jquery的代码中的实例部分.**
 ```html
  <!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>jQuery介绍</title>
</head>
<body>
    <!--jQuery字面上它的意思就是个动词了~-->
    <!--jQuery 是一个使用最管饭的js端插件
  集成了很多js的元素操作方法.事件方法.动画效果.ajax请求等等等功能
  框架是:很多插件的集合.可以解决一个完成项目的'所有问题'...
          一个框架可以解决一个项目'所有问题',但是你想把项目的一些更强大的方法解决了需要使用其他框架
        [underscore.js](http://www.css88.com/doc/underscore/)
        underscore封装了很多常用的操作方法
        
        jQuery.vakudate是一个表单验证插件,基于jQuery使用
        首要需要引用它.引用它需要先安装
        
        jquery版本问题,在jquery2.0之后不再支持ie的早起版本了如(i6/i7)
        如果你的页面需要支持ie早期版本.需要使用jquery小于2.0的版本
        安装jquery
        1.node install jQuery@版本号. 如果你不输入版本号是默认帮你安装最新版本的.安装请在终端内部安装
        2.bower install jQuery 也可以安装
        3.通过官方网站或者github下载 也是可以的
        4.可以使用cdn提供的值,引入在线版本..如(http://www.bootcdn.cn/)
    -->
    <!--创建一个span标签 设置它的class为sName-->
    <span id="sName">Edison</span>
    <div id="container">这是一个容器</div>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <script src="http://cdn.bootcss.com/jquery/3.0.0/jquery.min.js"></script>
    <script>
    //这种反法国是js中后期(最近)加入的方法.早期浏览器不支持(i6/i7)
    //借鉴了jQuery的元素选择方法
    console.log(document.querySelector('#sName'));
    
    console.log(jQuery);
    //$.fnjquery 获取版本号
    console.log($);
    //在使用jquery的时候,使用$和jquery关键字是等价的所有说 所以说$就等于jquery 一个字符代表六个英文字母.看你们个人爱好选择了..
    
    //在控制面板上输出下我们的$版本号吧
    console.log($.fn.jquery);
    
    //通过原生js选择Id为container 的标签元素
    console.log(document.querySelector('#container'));
    //上面的写法是会报错的null 这样是无效的.
    
    //通过使用$获取id为container的标签元素
    console.log($('#container'));
    
    /**
    通过Jquery元素选择获取的结果是一个jquery对象
    通过原生Js选择器获取的结果是一个js对象
    两者差别是很大的
    学习juqer的时候一定要把原生方法和jquery方法区分开来
    尽量避免两者的混用**/
    
    /***此方法是为原生js选择的元素添加click事件*/
    document.querySelector('#container').onclick = function(eve){alert('这是个容器')};
    
    //此方法是jquery选择的对象 添加click事件
    $('#container').click(function(){
    alert('这是一个container容器')})
    //两种添加事件的写法不一样不能混用
    
    for(var i=1;i<11;i++){
      var p = document.createElement('p');
      p.innerHTML = '这是第'+i+'行';
      document.body.appendChild(p);
    }
    
    //对页面中所有的p标签添加click事件
    $('p').click(function(){
    console.log(this);
      alert($(this).text());//通过jquery获取标签的文本内容
      alert(this.innerText);//在jquery方法中使用原生js方法
    })
    </script>
</body>
</html>
 ```
