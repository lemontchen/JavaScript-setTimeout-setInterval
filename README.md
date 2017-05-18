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

setTimeout(function () {

     that.html('<strong>60</strong>&nbsp;秒后可重发');
                       
      countDown();
                    
}, 1000);


用法二

 window.setInterval(function() {
            var day = 0,
                hour = 0,
                minute = 0,
                second = 0;//时间默认值          
            if (intDiff > 0) {
                day = Math.floor(intDiff / (60 * 60 * 24));  
                hour = Math.floor(intDiff / (60 * 60)) - (day * 24);
                minute = Math.floor(intDiff / 60) - (day * 24 * 60) - (hour * 60);
                second = Math.floor(intDiff) - (day * 24 * 60 * 60) - (hour * 60 * 60) - (minute * 60);
                intDiff--;
            }
            if (minute <= 9)
                minute = '0' + minute;
            if (second <= 9)
                second = '0' + second;
            //$('#day_show').html(day+"天"); 
            d = '#day_show'+k;
            a = '#hour_show'+k;
            b = '#minute_show'+k;
            c = '#second_show'+k;
            $(d).html(day+"天"); 
            $(a).html('<s></s>' + hour + '时');
            $(b).html('<s></s>' + minute + '分');
            $(c).html('<s></s>' + second + '秒');

        }, 1000);
