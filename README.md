<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">

<head>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />

<script src="https://code.jquery.com/jquery-3.1.1.min.js"></script>

<style type="text/css">

/*图片轮播*/

.box{

   margin-top: 20px;

   margin-left: 40px;

   height: 180px;

    background-color: white;

   position: relative;

   float: left;

}

.list{

   width: 300px;

   height: 150px;

   overflow: hidden;

   margin: 5px;

}

.next{

   right: 0;

}

.list li{

   position: absolute;

   top: 0;

   left: 0;

   list-style: none;

   opacity: 0;

   transition: all 0.3s ease-out;

}

.list img{

   border: 1px solid #DDD;

   float: left;

}

.list .p1{

   transform:translate3d(-100px,0,0) scale(0.70);

}

.list .p2{

   transform:translate3d(0px,0,0) scale(0.70);

   transform-origin:0 50%;

   opacity: 0.8;

   z-index: 2;

}

.list .p3{

   transform:translate3d(100px,0,0) scale(1);

   z-index: 3;

   opacity: 1;

}

.list .p4{

   transform:translate3d(200px,0,0) scale(0.70);

   transform-origin:100% 50%;

   opacity: 0.8;

   z-index: 2;

}

.list .p5{

   transform:translate3d(300px,0,0) scale(0.70);

}

.list .p6{

   transform:translate3d(400px,0,0) scale(0.70);

}

.list .p7{

   transform:translate3d(500px,0,0) scale(0.70);

}



.buttons{



 /*  width: 600px;*/

   height: 30px;

   bottom: 0;

   margin-left: 0px;

   text-align: center;

   padding-top: 10px;

}

.buttons a{

   display: inline-block;

   width: 35px;

   height: 5px;

   padding-top: 4px;

   cursor: pointer;

}



.buttons span{

   display: block;

   width: 35px;

   height: 1px;

   background: #DDDDDD;

}

.buttons .blue{

   background: #62a60a;

}

/*图片轮播结束*/

</style>

<title>图片轮播演示</title>

<script>

var $a=$(".buttons a");

var $s=$(".buttons span");

var cArr=[".list p7",".list p6",".list p5",".list p4",".list p3",".list p2",".list p1"];

var index=0;

window.onload=function(){

$a=$(".buttons a");

$s=$(".buttons span");

$(".next").click(

function(){

nextimg();

}

)

$(".prev").click(

function(){

previmg();

}

)

$(".buttons a").each(function(){

//通过底下按钮点击切换

$(this).click(function(){

var myindex=$(this).index();

var b=myindex-index;

if(b==0){

return;

}

else if(b>0) {

var newarr=cArr.splice(0,b);

cArr=$.merge(cArr,newarr);

$(".list li").each(function(i,e){

$(e).removeClass().addClass(cArr[i]);

})

index=myindex;

show();

}

else if(b<0){

cArr.reverse();

var oldarr=cArr.splice(0,-b)

cArr=$.merge(cArr,oldarr);

cArr.reverse();

$(".list li").each(function(i,e){

$(e).removeClass().addClass(cArr[i]);

})

index=myindex;

show();

}

})

})

}

//上一张

function previmg(){

cArr.unshift(cArr[6]);

cArr.pop();

//i是元素的索引，从0开始

//e为当前处理的元素

//each循环，当前处理的元素移除所有的class，然后添加数组索引i的class

$(".list li").each(function(i,e){

$(e).removeClass().addClass(cArr[i]);

})

index--;

if (index<0) {

index=6;

}

show();

}



//下一张

function nextimg(){

cArr.push(cArr[0]);

cArr.shift();

$(".list li").each(function(i,e){

$(e).removeClass().addClass(cArr[i]);

})

index++;

if (index>6) {

index=0;

}

show();

}

//改变底下按钮的背景色

function show(){

$($s).eq(index).addClass("blue").parent().siblings().children().removeClass("blue");

}



//点击class为p2的元素触发上一张照片的函数

$(document).on("click",".list .p2",function(){

previmg();

return false;//返回一个false值，让a标签不跳转

});



//点击class为p4的元素触发下一张照片的函数

$(document).on("click",".list .p4",function(){

nextimg();

return false;

});



//鼠标移入box时清除定时器

$(".box").mouseover(function(){

clearInterval(timer);

})



//鼠标移出box时开始定时器

$(".box").mouseleave(function(){

timer=setInterval(nextimg,4000);

})



//进入页面自动开始定时器

timer=setInterval(nextimg,4000);



   </script>

</head>



<body>

<div  class="box">

  <div class="list" >

     <ul>

       <li class="p1"><a href=""><img src="/static/images/survey_02.png" alt=""   width="300" height="150" /></a></li>

                     <li class="p2"><a href=""><img src="/static/images/survey_02.png" alt=""   width="300" height="150"  /></a></li>
