#  《通信软件开发与应用》
##一、做的什么
###1.1 任务要求：
任务一：构建一个静态或动态网站。以下要求中任选A或B，要求如下：
A. 静态网站
采用纯 CSS 或你喜欢的任何 CSS 框架如 Bootstrap、MDB、Tailwind 等构建一个主题自选且不少于5个页面（Web Page）的网站
B. 动态网站
使用任何一个前端框架如 Angular 等进行某应用（如英雄之旅等）的开发，需要有 CRUD 即增删改查功能并有一定的样式。
无论你选择静态还是动态网站，该网站都需部署到你喜欢的网站托管服务器上如 Gitpage 等（Angular项目可参阅 https://angular.cn/guide/deployment）。
该网站需放置你的结业报告（要求见任务二）。
任务二：撰写结业报告，要求如下：
（1） 题目为《通信软件开发与应用》课程结业报告；
（2） 报告需阐述：做的什么、开发过程、遇到的问题、如何解决、哪些未解决、总结；
（3） 该报告以 Web 页面的形式呈现，从你上面开发的网站中可访问到。
###1.2 主题
设计一个分享展示肖战图片的网页
##二.效果展示
###2.1
![avater](https://img-blog.csdnimg.cn/2c19defd720446658099fa378928e763.png)
###2.2
![avater](https://img-blog.csdnimg.cn/82c042eebe344ebd9d322df7e10db213.png)
###2.3
![avater](https://img-blog.csdnimg.cn/7be6dd999310429490ebbdc5347aa99c.png)
###2.4
![avater](https://img-blog.csdnimg.cn/d19b795f3ec548c78b3dc48df24e9271.png)
###2.5
![avater](https://img-blog.csdnimg.cn/c892dde8f28544aebeff04ec80d9e5a4.png)
##三、实现过程
###3.1 主页设计
登录界面html
![avater](https://img-blog.csdnimg.cn/2c19defd720446658099fa378928e763.png)
```
<!DOCTYPE html>
<html lang="en">
<head>

    <meta charset="UTF-8">
    <title>虾壳</title>
    <link rel="shortcut icon" href="https://mat1.gtimg.com/qqcdn/qqindex2021/favicon.ico"/>
    <link rel="stylesheet" href="start.css">
    <style type="../css/start.css">
        @import "../css/start.css";
    </style>
</head>
<body>



<div class="top">遇见彩虹 吃定彩虹</div>

<div align="center">
    <div class="pic">
        <img src="https://img2.woyaogexing.com/2022/02/21/5831daf62f54429cbd22c9cd076acd37!400x400.jpeg" width="100" height="100" alt="头像">
    </div>
    <div class="loginbg">
        <p class="blue">虾壳</p>
        账号：
        <input id="userName" class="user" type="text"> <br>
        密码：
        <input id="password" class="user" type="password"><br>
        <button id="loginBtn" class="login" type="button">
            <a href="mian.html">点击进入</a>
        </button><br>

    </div>


</div>

</body>
</html>

```
登录css

```
.body {
    margin: 0;
    padding: 0;
    background: #111111;
    color: #d9d9d9;
    /*background-image: url("https://img2.baidu.com/it/u=2352880048,3169510647&fm=253&fmt=auto&app=138&f=JPEG?w=575&h=346");*/

}

.top {
    background: #000;
    width: 100%;
    height: 35px;
    color: #17A1FF;
    font-size: 18px;
    line-height: 35px;
    text-align: center;
}

.loginbg {
    width: 30%;
    background: #000;
    margin: 20px 0 0px 0;
    border-radius: 30px 30px 30px 30px;
    /*background-image: url("http://img.netbian.com/file/2022/0223/010035r3aFr.jpg");*/
    /*opacity:0.1;*/
}

.blue {
    color: #17A1FF;
    font-size: 18px;
    line-height: 50px;

}

.user_ico {

    background-image: url("http://v.bootstrapmb.com/2021/8/apbk210845 /img/login_ico.png");
    background-repeat: no-repeat;
    background-position: -125px -34px;
    margin: 10px 13px;
    position: absolute;
}

.user {
    width: 50%;
    height: 30px;
    border-width: 1px;
    border-radius: 20px 20px 20px 20px;
    margin: 5px 0 20px 5px;
    color: #007DDB;

    /*border: rgba(255,255,255,0.2) 2px solid !important;*/
    /*background-color:transparent*/
    background-color: #d9d9d9;
}

.login {
    text-align: center;
    font-size: 20px;
    line-height: 50px;
    width: 50%;
    height: 50px;
    border-radius: 10px 10px 10px 10px;
    margin: 15px 0 20px 55px;
    background-color: #007DDB;
    color: #FFFFFF;
}

.pic {
    margin: 10px auto;
    margin: 150px 0 0px 0;
}

img {
    /*border-radius: 20px;*/

    border-radius: 50%
}
```
主界面导航条
![avater](https://img-blog.csdnimg.cn/82c042eebe344ebd9d322df7e10db213.png)
```
<div class="nav">
    <!--href="#":阻断a标签跳转刷新页面-->
    <ul>
        <li><a href="#">首页</a></li>
        <li><a href="picture.html">图片</a></li>
        <li><a href="video.html">视频</a></li>
        <li><a href="#">结业报告</a></li>
    </ul>
</div>
<h1>人物简历——肖战</h1>
			<div id="nav">
				<ul>
					<li>
						<a href="#info">基本信息</a>
					</li>
					<li>
						<a href="#early">早年经历</a>
					</li>
					<li>
						<a href="#career">演艺经历</a>
					</li>
					<li>
						<a href="#prize">获奖记录</a>
					</li>
					<li>
						<a href="#contribution">社会活动</a>
					</li>
					<li>
						<a href="#contact">联系信息</a>
					</li>
				</ul>
			</div>
```
展示图片界面
![avater](https://img-blog.csdnimg.cn/d19b795f3ec548c78b3dc48df24e9271.png)
```
<body>
 
 
<div class="container marketing">
<section id="blog-landing">

<article class="white-panel wow slideInLeft" data-wow-duration="0.5s" data-wow-delay="0.5s"> 
<img src="img/0.jpg" alt="ALT">
<h1>
<a href="#">life</a>
</h1>

<p>就算生活把屋檐压的再低，也总会有另一片的天空</p>
</article>

```
视频播放界面
![avater](https://img-blog.csdnimg.cn/c892dde8f28544aebeff04ec80d9e5a4.png)
html
```
  <!-- custom css file link  -->
   <link rel="stylesheet" href="video.css">

</head>
<body>
   
<div class="container">

   <div class="main-video-container">
      <video src="video/tianwen.mp4" loop controls class="main-video"></video>
      <h3 class="main-vid-title">house flood animation</h3>
   </div>

   <div class="video-list-container">

      <div class="list active">
         <video src="video/tianwen.mp4" class="list-video"></video>
         <h3 class="list-title">天问</h3>
      </div>

      <div class="list">
         <video src="video/honghai.mp4" class="list-video"></video>
         <h3 class="list-title">八秒红海</h3>
      </div>
```
css
```
*{
   font-family: 'Poppins', sans-serif;
   margin:0; padding:0;
   box-sizing: border-box;
   outline: none; border:none;
   text-decoration: none;
   text-transform: capitalize;
}

body{
   background-color: coral;
   padding:20px;
}

.container{
   max-width: 1200px;
   margin:100px auto;
   display: flex;
   flex-wrap: wrap;
   align-items: flex-start;
   gap:20px;
}

.container .main-video-container{
   flex:1 1 700px;
   border-radius: 5px;
   box-shadow: 0 5px 15px rgba(0,0,0,.1);
   background-color: #fff;
   padding:15px;
}

.container .main-video-container .main-video{
   margin-bottom: 7px;
   border-radius: 5px;
   width: 100%;
}

.container .main-video-container .main-vid-title{
   font-size: 20px;
   color:#444;
}

.container .video-list-container{
   flex:1 1 350px;
   height: 485px;
   overflow-y: scroll;
   border-radius: 5px;
   box-shadow: 0 5px 15px rgba(0,0,0,.1);
   background-color: #fff;
   padding:15px;
}

.container .video-list-container::-webkit-scrollbar{
   width: 10px;
}

.container .video-list-container::-webkit-scrollbar-track{
   background-color: #fff;
   border-radius: 5px;
}

.container .video-list-container::-webkit-scrollbar-thumb{
   background-color: #444;
   border-radius: 5px;
}

.container .video-list-container .list{
   display: flex;
   align-items: center;
   gap:15px;
   padding:10px;
   background-color: #eee;
   cursor: pointer;
   border-radius: 5px;
   margin-bottom: 10px;
}

.container .video-list-container .list:last-child{
   margin-bottom: 0;
}

.container .video-list-container .list.active{
   background-color: #444;
}

.container .video-list-container .list.active .list-title{
   color:#fff;
}

.container .video-list-container .list .list-video{
   width: 100px;
   border-radius: 5px;
}

.container .video-list-container .list .list-title{
   font-size: 17px;
   color:#444;
}
@media (max-width:1200px){

   .container{
      margin:0;
   }

}

@media (max-width:450px){

   .container .main-video-container .main-vid-title{
      font-size: 15px;
      text-align: center;
   }

   .container .video-list-container .list{
      flex-flow: column;
      gap:10px;
   }

   .container .video-list-container .list .list-video{
      width: 100%;
   }

   .container .video-list-container .list .list-title{
      font-size: 15px;
      text-align: center;
   }

}
```
##四.遇到的问题，及解决方案
###4.1
问题：在视频播放界面有的视频播放不了
已解决；
原因：有的视频的格式不对，必须要MP4格式的视频才能播放
##五.总结
通过一学期的学习，我基本了解了html和css，可以自己运用这些知识，但是对于后面讲的框架以及anguler等的运用我还不太熟悉，我会利用课后时间继续深入学习。
在进行问题分析时，我们首先需要找到问题的所在，从大方面深入到小的方面，可以采用试错的方法，逐步分析，这相应的需要我们熟悉每一个版块的功能，在细节上找到问题所在。