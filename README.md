<!DOCTYPE html>
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
    <img class="img-slide img1" src="https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fpic.jj20.com%2Fup%2Fallimg%2F1111%2F06041Q43S7%2F1P604143S7-9.jpg&refer=http%3A%2F%2Fpic.jj20.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1644316528&t=b8f919e19c4868e50062b586da5cf41f" alt="1">
    <img class="img-slide img2" src="https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fup.enterdesk.com%2Fedpic_source%2F25%2Fbb%2F55%2F25bb5526e31389a07094cc12dee17453.jpg&refer=http%3A%2F%2Fup.enterdesk.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1644316562&t=3f216b7d013b9ec0ee17ed57f5da3471" alt="2">
    <img class="img-slide img3" src="https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fpic.jj20.com%2Fup%2Fallimg%2F1111%2F06041Q43S7%2F1P604143S7-9.jpg&refer=http%3A%2F%2Fpic.jj20.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1644316528&t=b8f919e19c4868e50062b586da5cf41f" alt="3">
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
版权声明：本文为CSDN博主「limakrim丶」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/qq_45225221/article/details/122397056
