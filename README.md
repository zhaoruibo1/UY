<SCRIPT LANGUAGE="JavaScript">
function password() {
var testV = 1;
var pass1 = prompt('输入暗号');
while (testV < 3) {
if (!pass1) 
history.go(-1);
if (pass1 == "渣男") {
alert('暗号正确，果然是我媳妇!');
break;
} 
testV+=1;
var pass1 = 
prompt('哼，不对');
}
if (pass1!="password" & testV ==3)               
history.go(-1);
return " ";
}      
document.write(password());
</SCRIPT>

<meta name="keywords" content="我爱你" />
<meta name="description" content="- www.zrblovewyy.我爱你" />
<body ondragstart="window.event.returnValue=false" oncontextmenu="window.event.returnValue=false" onselectstart="event.returnValue=false">
<META http-equiv="Content-Type" content="text/html; charset=utf-8">
		 <TITLE>爱情树丨 www.zrblovewyy.我爱你</TITLE>	             <LINK href="shuju/default.css" 
rel="stylesheet" type="text/css">		 
<SCRIPT src="shuju/jquery.min.js" type="text/javascript"></SCRIPT>
		 
<SCRIPT src="shuju/jscex.min.js" type="text/javascript"></SCRIPT>
		 
<SCRIPT src="shuju/jscex-parser.js" type="text/javascript"></SCRIPT>
		 
<SCRIPT src="shuju/jscex-jit.js" type="text/javascript"></SCRIPT>
		 
<SCRIPT src="shuju/jscex-builderbase.min.js" type="text/javascript"></SCRIPT>
		 
<SCRIPT src="shuju/jscex-async.min.js" type="text/javascript"></SCRIPT>
		 
<SCRIPT src="shuju/jscex-async-powerpack.min.js" type="text/javascript"></SCRIPT>
		 
<SCRIPT src="shuju/functions.js" type="text/javascript" charset="utf-8"></SCRIPT>
		 
<SCRIPT src="shuju/love.js" type="text/javascript" charset="utf-8"></SCRIPT>
	     
<STYLE type="text/css">
<!--
.STYLE1 {color: #666666}
-->
        
-->
        </STYLE>   
<DIV id="main">
<DIV id="wrap">
<DIV id="text">
<DIV id="code"><FONT color="pink"><SPAN class="say">* 
亲爱的，往这看，mua~</SPAN><BR><SPAN class="say"></SPAN><BR><SPAN class="say">* 
世界上最好闻的味道 就是抱着你时 你身上的味道。</SPAN><BR><SPAN class="say"></SPAN><BR><SPAN class="say">* 
我会用以后的生命好好的疼你，宠你，爱你。</SPAN><BR><SPAN class="say"></SPAN><BR><SPAN 
class="say">* 不管发生什么事情，不论有着什么样的争吵。我都会一如继往的爱你，不会有一个不字。</SPAN><BR><SPAN class="say"></SPAN><BR><SPAN 
class="say">* 快乐、欢笑、悲伤、泪水……你快乐我们一起快乐，你难过是你最大的依靠，无论如何我都会和你一同度过！ 
</SPAN><BR><SPAN class="say"></SPAN><BR><SPAN class="say">* 
等我们有了足够的条件时，和你一起，完成你做老板娘的终极梦想</SPAN><BR><SPAN 
class="say"></SPAN><BR><SPAN class="say">* 
幸福是一辈子的事，经得起重重考验，才能幸福的度过余生。我会用自己的双手为你换来一个幸福的未来！</SPAN><BR><SPAN 
class="say"></SPAN><BR><SPAN class="say">* 
伴着音乐，我想对你说，我爱你！我要照顾你一辈子！</SPAN><BR><SPAN class="say"></SPAN><BR><SPAN class="say"><SPAN 
class="space"></SPAN> -- 爱你的 赵瑞博--</SPAN>			   </FONT>
<P></P></DIV></DIV>
<DIV id="clock-box">爱你的...                
   
<DIV id="clock"></DIV></DIV><CANVAS width="1100" height="680" 
id="canvas"></CANVAS>             </DIV></DIV>
<SCRIPT>

    (function(){
        var canvas = $('#canvas');
		
        if (!canvas[0].getContext) {
            $("#error").show();
            return false;
        }

        var width = canvas.width();
        var height = canvas.height();
        
        canvas.attr("width", width);
        canvas.attr("height", height);

        var opts = {
            seed: {
                x: width / 2 - 20,
                color: "rgb(190, 26, 37)",
                scale: 2
            },
            branch: [
                [535, 680, 570, 250, 500, 200, 30, 100, [
                    [540, 500, 455, 417, 340, 400, 13, 100, [
                        [450, 435, 434, 430, 394, 395, 2, 40]
                    ]],
                    [550, 445, 600, 356, 680, 345, 12, 100, [
                        [578, 400, 648, 409, 661, 426, 3, 80]
                    ]],
                    [539, 281, 537, 248, 534, 217, 3, 40],
                    [546, 397, 413, 247, 328, 244, 9, 80, [
                        [427, 286, 383, 253, 371, 205, 2, 40],
                        [498, 345, 435, 315, 395, 330, 4, 60]
                    ]],
                    [546, 357, 608, 252, 678, 221, 6, 100, [
                        [590, 293, 646, 277, 648, 271, 2, 80]
                    ]]
                ]] 
            ],
            bloom: {
                num: 700,
                width: 1080,
                height: 650,
            },
            footer: {
                width: 1200,
                height: 5,
                speed: 10,
            }
        }

        var tree = new Tree(canvas[0], width, height, opts);
        var seed = tree.seed;
        var foot = tree.footer;
        var hold = 1;

        canvas.click(function(e) {
            var offset = canvas.offset(), x, y;
            x = e.pageX - offset.left;
            y = e.pageY - offset.top;
            if (seed.hover(x, y)) {
                hold = 0; 
                canvas.unbind("click");
                canvas.unbind("mousemove");
                canvas.removeClass('hand');
            }
        }).mousemove(function(e){
            var offset = canvas.offset(), x, y;
            x = e.pageX - offset.left;
            y = e.pageY - offset.top;
            canvas.toggleClass('hand', seed.hover(x, y));
        });

        var seedAnimate = eval(Jscex.compile("async", function () {
            seed.draw();
            while (hold) {
                $await(Jscex.Async.sleep(10));
            }
            while (seed.canScale()) {
                seed.scale(0.95);
                $await(Jscex.Async.sleep(10));
            }
            while (seed.canMove()) {
                seed.move(0, 2);
                foot.draw();
                $await(Jscex.Async.sleep(10));
            }
        }));

        var growAnimate = eval(Jscex.compile("async", function () {
            do {
    	        tree.grow();
                $await(Jscex.Async.sleep(10));
            } while (tree.canGrow());
        }));

        var flowAnimate = eval(Jscex.compile("async", function () {
            do {
    	        tree.flower(2);
                $await(Jscex.Async.sleep(10));
            } while (tree.canFlower());
        }));

        var moveAnimate = eval(Jscex.compile("async", function () {
            tree.snapshot("p1", 240, 0, 610, 680);
            while (tree.move("p1", 500, 0)) {
                foot.draw();
                $await(Jscex.Async.sleep(10));
            }
            foot.draw();
            tree.snapshot("p2", 500, 0, 610, 680);

            // 会有闪烁不得意这样做, (＞﹏＜)
            canvas.parent().css("background", "url(" + tree.toDataURL('image/png') + ")");
            canvas.css("background", "#ffe");
            $await(Jscex.Async.sleep(300));
            canvas.css("background", "none");
        }));

        var jumpAnimate = eval(Jscex.compile("async", function () {
            var ctx = tree.ctx;
            while (true) {
                tree.ctx.clearRect(0, 0, width, height);
                tree.jump();
                foot.draw();
                $await(Jscex.Async.sleep(25));
            }
        }));

        var textAnimate = eval(Jscex.compile("async", function () {
		    var together = new Date();
		    together.setFullYear(2017,09 ,20); //时间年月日			
		    together.setHours(07);						//小时	
		    together.setMinutes(46);//分钟					
		    together.setSeconds(0);					//秒前一位
		    together.setMilliseconds(55);				//秒第二位

		    $("#code").show().typewriter();
            $("#clock-box").fadeIn(500);
            while (true) {
                timeElapse(together);
                $await(Jscex.Async.sleep(1000));
            }
        }));

        var runAsync = eval(Jscex.compile("async", function () {
            $await(seedAnimate());
            $await(growAnimate());
            $await(flowAnimate());
            $await(moveAnimate());

            textAnimate().start();

            $await(jumpAnimate());
        }));

        runAsync().start();
    })();
    </SCRIPT>    
    <div class="bg2">	
		<div class="main">
			<footer style="line-height:40px">
                <div id="copyright">
                    <div align=" center"><span style="font-size:40px;font-weight:bold;color:pink;">欢迎来到王悠阳&赵瑞博的小窝
		    <div class="bg3">	
		<div class="main">
			<footer style="line-height:-50px">
                <div id="copyright">
                    <div align=" center"><a href="shuju/首页.html" style="font-style: normal; font-weight: 400;"><span style="font-size:20px;font-weight:bold;color:pink;">首页
	<div class="bg1">	
		<div class="main">
			<footer style="line-height:-50px">
                <div id="copyright">
                    <div align=" center"><a href="shuju/新建文本文档.html" style="font-style: normal; font-weight: 400;"><span style="font-size:20px;font-weight:bold;color:pink;">甜蜜时光      	
	   
<audio id="bgmMusic" src="shuju\1.mp3" preload="auto" type="audio/mp3" autoplay loop></audio>

