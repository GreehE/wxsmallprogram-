微信小程序01——简单的图书信息页面设计
====
代码片段展示：
----
* index.wxml
```
<!-- 第一个区域：图片 -->
<view>
  <image src="https://ss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=624637620,2003969594&fm=26&gp=0.jpg"></image>
</view>
<!-- 第二个区域：文字 -->
<view class="bookintro">
  <h>书名：</h>
   <text>Becoming</text>
  <h>作者：</h>
   <text>Michelle Obama</text>
  <h>出版社：</h>
   <text>天地出版社</text>
  <h>简介：</h>
   <text>《Becoming》详细记录了米歇尔生活中的所有重要细节，包括在芝加哥南部度过的童年、成年后的职业生涯和作为母亲的经历，以及她在白宫的经历、在公共卫生领域展开的运动，奥巴马执政中的重要时刻。</text>
  <h>章节信息：</h>
   <p style="white-space:pre-wrap; line-height:50rpx;">
    目录
    序
    Part I 成为我
    Part II 成为我
    Part III 成为更多
    后记
    致谢</p>
  <!-- <button open-type="getUserInfo"   
bindgetuserinfo="getMyInfo">点击前往购买</button> -->
</view>
```
* index.wxss
```
/* 样式设计 */
view{
  background-color:rgb(234, 225, 241); 
}
.bookintro{
  height: 100vh; /*高100视窗，这里写100%是无效的*/
  display: flex; /*flex布局方法*/
  flex-direction: column; /*垂直布局*/
  align-items:baseline; /*水平居左边*/
  justify-content:left;
}
image{    /*全部image采用一个样式*/  /*image采用abc的样式*/
 border: 10rpx solid #716981;
 margin-top: 30rpx;
 margin-left: 110rpx;
 width: 500rpx;/*图片宽带*/
 /*border-radius: 45%;/*四个角变为圆角形状*/
 align-items:center; 
 height: 40vh;
}
h{
  height: 50rpx;
  font-size: 40rpx;
  color:rgb(90, 90, 119);
  font-weight: bold;
  margin: 10rpx;
}
text{
  margin-left: 10rpx;
  font-size: 30rpx;
}
p{
  font-size: 30rpx;
  margin-left: 10rpx;

}
```
* 小程序全局布局，如导航栏文字颜色，背景颜色：
```
{
  "pages": [
    "pages/index/index"
  ],
  "window": {
    "navigationBarBackgroundColor": "#b1abbd",
    "navigationBarTextStyle": "black",
    "navigationBarTitleText": "图书信息"
  },
  "sitemapLocation": "sitemap.json"
}
```


