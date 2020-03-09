移动开发第二周课后作业
===
——列表渲染，条件渲染
---
* 基于上周作业的代码优化：
>1.在项目中新建一个数据文件info.js，存放目录信息：
```
var infos =[
  {
    "id":"1",
    "content":"目录"
  },
  {
    "id": "2",
    "content": "序"
  },
  {
    "id": "3",
    "content": "Part I 成为我"
  },
  {
    "id": "4",
    "content": "Part II 成为我"
  },
  {
    "id": "5",
    "content": "Part III 成为更多"
  },
  {
    "id": "6",
    "content": "后记"
  },
  {
    "id": "7",
    "content": "致谢"
  }
]
module.exports = {infos};
```
>2.然后在需要渲染的页面js文件里，引入刚才的数据：
```
var jsonData = require('/infos.js');
Page({
  data:{

      },
      onLoad: function(){
        var that = this;
        this.setData({
          infos: jsonData.infos
        });
      }
})
```
>3.在主页面index.wxml文件里，对需要渲染的部分输出：
```
...
<!-- 第三个区域：目录列表 -->
   <view wx:for="{{infos}}" wx:for-item="item2" wx:key="id" >
  <text>
  {{index+1}}、{{item2.content}}</text>
  </view>
  ```
  对比原来的代码：
  ```
  <!--<p style="white-space:pre-wrap; line-height:50rpx;">
    目录
    序
    Part I 成为我
    Part II 成为我
    Part III 成为更多
    后记
    致谢</p>-->
    ```
