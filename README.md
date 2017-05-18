# JavaScript-setTimeout-setInterval
JavaScript定时设置

1、只执行一次的定时器 

<script>
  //定时器 异步运行
  function hello(){
    alert("hello");
  }

//使用方法名字执行方法

var t1 = window.setTimeout(hello,1000);

var t2 = window.setTimeout("hello()",3000);//使用字符串执行方法

window.clearTimeout(t1);//去掉定时器

</script> 

2、重复执行的定时器

<script>

function hello(){

  alert("hello");
 
 }

//重复执行某个方法

var t1 = window.setInterval(hello,1000);

var t2 = window.setInterval("hello()",3000);

//去掉定时器的方法

window.clearInterval(t1);

</script>

参考链接：http://www.jb51.net/article/47819.htm


JQ用法

setTimeout(function ()
{

     代码段
                    
}, 1000);


用法二

 window.setInterval(function() 
 {
 
  代码段           

 }, 1000);
