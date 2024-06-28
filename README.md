# Lucie
<!--慕课网js初级练习-->
<!DOCTYPE HTML>
<html>
<head>
<meta http-equiv="Content-Type" Content="text/html; charset=utf-8" />
<title>javascript</title>
<style type="text/css">
body{font-size:12px;}
#txt{
    height:400px;
    width:600px;
	border:#333 solid 1px;
	padding:5px;}
p{
	line-height:18px;
	text-indent:2em;}
</style>
</head>
<body>
  <h2 id="con">JavaScript课程</H2>
  <div id="txt"> 
     <h5>JavaScript为网页添加动态效果并实现与用户交互的功能。</h5>
        <p>1. JavaScript入门篇，让不懂JS的你，快速了解JS。</p>
        <p>2. JavaScript进阶篇，让你掌握JS的基础语法、函数、数组、事件、内置对象、BOM浏览器、DOM操作。</p>
        <p>3. 学完以上两门基础课后，在深入学习JavaScript的变量作用域、事件、对象、运动、cookie、正则表达式、ajax等课程。</p>
  </div>
  <form>
  <!--当点击相应按钮，执行相应操作，为按钮添加相应事件-->
    <input type="button" onClick="color()" value="改变颜色" >  
    <input type="button" onClick="high()" value="改变宽高" >
    <input type="button" onClick="hide()" value="隐藏内容" >
    <input type="button" onClick="play()" value="显示内容" >
    <input type="button" onClick="setting()" value="取消设置" >
  </form>
  <script type="text/javascript">
//定义"改变颜色"的函数
function color(){
var main=document.getElementById("txt");
var title=document.getElementById("con");
title.style.color="pink";
main.style.color="red";
main.style.backgroundColor="blue";
}
function high(){
//定义"改变宽高"的函数
var main=document.getElementById("txt");
var title=document.getElementById("con");
main.style.width="300px";
main.style.height="600px";
title.style.width="100px";
}
function hide(){
//定义"隐藏内容"的函数
var main=document.getElementById("txt");
main.style.display="none";
}
function play(){
//定义"显示内容"的函数
var main=document.getElementById("txt");
main.style.display="block";
}
function setting(){
//定义"取消设置"的函数
var mymessage = confirm("are you sure cancel setting?");
if(mymessage==true)
{
    var main=document.getElementById("txt");
    var title=document.getElementById("con");
    main.removeAttribute('style');
    title.removeAttribute('style');
}
else
{
    alert("no change");
}
}
  </script>
</body>
</html>
