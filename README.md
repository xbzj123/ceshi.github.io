
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title></title>
    <style type="text/css">

        .imgBox{
            border-top: 2px solid cadetblue;
            width: 100%;
            height: 250px;
            margin: 0 auto;

        }

        .imgBox img{
            width: 100%;
            height: 250px;
            margin: 0 auto;
            padding-top: 30px;

        }

        .img1{
            display: block;
        }

        .img2{
            display: none;
        }

        .img3{
            display: none;
        }
    </style>
</head>
<body>
<p></p>
<div class="imgBox">
    <img class="img-slide img1" src="https://pic.imgdb.cn/item/62931864094754312914ff79.jpg" alt="1">
    <img class="img-slide img2" src="https://pic.imgdb.cn/item/6294dee30947543129597092.jpg" alt="2">
    <img class="img-slide img3" src="https://pic.imgdb.cn/item/62a86a4e09475431298c7ac5.jpg" alt="3">
</div>
</body>
<script type="text/javascript">
    var index=0;
    //效果
    function ChangeImg() {
        index++;
        var a=document.getElementsByClassName("img-slide");
        if(index>=a.length) index=0;
        for(var i=0;i<a.length;i++){
            a[i].style.display='none';
        }
        a[index].style.display='block';
    }
    //设置定时器，每隔两秒切换一张图片
    setInterval(ChangeImg,3000);
</script>
</html>

[![Pull Requests Welcome](https://img.shields.io/badge/%E2%9C%9F-%E4%B8%BB%E6%97%A5%E8%AF%81%E9%81%93-brightgreen)](https://xbzj123.github.io/Sunday.github.io/)
[![first-timers-only Friendly](https://img.shields.io/badge/%E2%9C%9F-%E6%9F%A5%E7%BB%8F%E5%88%86%E4%BA%AB-yellowgreen)](https://xbzj123.github.io/Bible.github.io/)
[![Open Source Helpers](https://img.shields.io/badge/%E2%9C%9F-%E5%88%9D%E4%BF%A1%E6%A0%BD%E5%9F%B9-orange)](https://xbzj123.github.io/chuxin.github.io/)
[![Setup Automated](https://img.shields.io/badge/%E2%9C%9F-%E5%BB%BA%E8%AE%BE%E4%B8%AD%E2%80%A6%E2%80%A6-blue)](https://www.asuswebstorage.com/navigate/a/#/s/BE676B2CA5B3400CA7273ABFBB76BEFDY)
