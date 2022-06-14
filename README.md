
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>轮播图</title>
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
<p>图片轮播</p>
<div class="imgBox">
    <img class="img-slide img1" src="https://pic.imgdb.cn/item/62931864094754312914ff79.jpg" alt="1">
    <img class="img-slide img2" src="https://pic.imgdb.cn/item/62931864094754312914ff79.jpg" alt="2">
    <img class="img-slide img3" src="https://pic.imgdb.cn/item/62931864094754312914ff79.jpg" alt="3">
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

————————————————
