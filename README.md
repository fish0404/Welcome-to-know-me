<!DOCTYPE html>
<html lang="en">
<head>
    <!--meta 单标签 用来引入或声明一些内容-->
    <meta charset="UTF-8">
    <!--title 标题标签-->
    <title>About Me</title>
    <style>
        body{
            /*边界看宽度默认为8,在这里初始值设为零*/
            margin: 0;
            font-family: 楷体;
        }
        nav{
            width: 100%;
            height: 140px;
            /*定位方式: 固定位置*/
            position: fixed;
            top: 0;
            background-color: white;
            z-index: 1000;
        }
        /*找到nav标签下 div标签后代选择器 ，可以找到nav下的所有的div标签*/
        nav div{
            width: 1000px;
            height: 64px;
            /*块元素居中*/
            margin:0 auto;
        }
        #logo{
            width: 216px;
            /*相对定位,位置微调*/
            position: relative;
            top: 7px;
            left: 15px;
        }
        ul{
            float: right;
            margin: 0;
            /*左内边距设为零*/
            padding-left: 0;
        }
        li{
            float: left;
            /*设置列表项的前缀为none*/
            list-style: none;
            margin-right: 30px;
        }
        li a{
            line-height: 64px;
            /*去除超链接下划线*/
            text-decoration: none;
            color: black;
        }
        li a:hover{
            color: brown;
        }
        #header{
            /*图片宽度设为100%*/
            width: 100%;
        }
        main {
            width: 1000px;
            margin:0 auto;
        }
        /*只找到父子关系的标签找到section下img标签，不会找到孙级标签*/
        section > img {
            width: 1000px;
        }
        p {
            color: brown;
            /*文本首行缩进2个字符*/
            text-indent: 2em;
        }
        h2 {
            color: brown;
        }
        #myclassmate {
            width: 1000px;
            height: 630px;
            background-image: url('personage/classmates.jpg');
            background-size: 1000px 630px;
            /*relative 相对的 相对定位 */
            /*1. 相对自己原来的位置做位置的微调
            2.让该标签下的子标签做绝对定位时，以该标签为参考物调整，而不再是以浏览器边框为参考物*/
            position: relative;
        }
        #myclassmate img{
            border:2px white solid;
            border-radius: 50%;
            /*absolute1.绝对定位的元素会被浮起来，原来的位置会被后面的元素侵占*/
            position: absolute;
        }
        /*找到div下的第1个子标签*/
        #myclassmate img:nth-child(1){
            width: 200px;
            top: 100px;
            left: 100px;
        }
        /*找到div下的第2个子标签*/
        #myclassmate img:nth-child(2){
            width: 270px;
            top: 260px;
            left: 360px;
        }
        /*找到div下的第3个子标签*/
        #myclassmate img:nth-child(3){
            width: 230px;
            top: 100px;
            right: 60px;
        }
    </style>
</head>
<body>
    <!--加载音频文件-->
    <audio src="葫芦娃.mp3" autoplay></audio>
    <!--加载视频文件-->
    <video src=""></video> 
    <!--navigation 导航 标记网页中的导航条 块元素-->
    <nav>
        <div>
            <h1>MXY</h1>
            <!--ul无序列表 li 列表元素-->
            <ul>
                <!--实现点击首页标签跳转到指定界面-->
                <!--a标签  超链接标签-->
                <li><a href="#header">Home</a></li>
                <li><a href="#html5">HTML5</a></li>
                <li><a href="#classmates">My Classmates</a></li>
                <li><a href="#hometown">My hometown</a></li>
                <li><a href="#myschool">My College</a></li>
                <li><a href="#myself">It's me</a></li>
            </ul>
        </div>
    </nav>
    <img id="header" src="a.jpg">
    <!--main 元素 标记网页中的主要部分内容-->
    <main>
        <!--p标签，用来标记网页中的段落内容！-->
        <p>“Where there is a will, there is a way”</p>
        <!--section 组件、模块, 块元素-->
        <section id="html5">
            <img src="personage/html5.jpg" alt="html5.jpg">
            <p>“从小就喜欢学习,感觉自己的自学能力超强,也喜欢把自己学会的知识分享给大家。我希望自己能够成为一个好老师,把每一个同学·都教好,让他们都能有所成就。我认为一个好老师不仅要有较好的技术,也要对学生严格要求。放任不管只有部分同学能安心学习,严格要求才能保证绝大多数同学都能稳下心来好好学习。”</p>
        </section>
        <section id="classmates">
            <h2>我的同学</h2>
            <div id="myclassmate">
                <img src="personage/wf.png" alt="">
                <img src="personage/lry.jpg" alt="">
                <img src="personage/ldh.jpg" alt="">
            </div>
            <p>“王菲、刘若英、刘德华都是我的同学。”</p>
        </section>
        <section id="hometown">
            <h2>我的家乡</h2>
            <img src="personage/hometown.JPG" alt="hometown.jpg">
            <p>我的家乡是个美丽的城市。</p>
        </section>
        <section id="myschool">
            <h2>我的学校</h2>
            <img src="personage/lzu.jpg" alt="lzu.jpg">
            <p>我的学校是一所很好的学校。</p>
        </section>
    </main>
    <hr>
    <!--声明个人版权-->
    <p id="myself" style="text-align: center;">&copy;木之易，版权所有。</p>
</body>
</html>
