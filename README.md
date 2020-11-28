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
            height: 250px;
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
            /*1. 相对自己原来的位置做位置
