<template>
    <div class="detail-page">
       <div class="video">
         <video src="" controls="controls">
         </video>
         <router-link to="/">
             <div class="video-back"> &lt; </div>
         </router-link>
       </div>
       <ul class="nav">
         <li v-for="(item,index) in arr" :key="index">{{item}}</li>
       </ul>
       <div class="title">
         <h1>{{title}}</h1>
         <p>{{des}}</p>
         <img src="../assets/arr.png"></img>
       </div>

       <ul class="question">
         <li v-for="(item, index) in arrQuestion" :key="index">
            <h1>{{arrTitle[index]}}</h1>
            <p v-html="item"></p>
         </li>
       </ul>
       <footer></footer>
    </div>
</template>
<script>
export default{
  data () {
    return {
      arr: [],
      title: '',
      des: '',
      arrQuestion: [],
      arrTitle: ['课程须知', '老师告诉你能学到什么？']
    }
  },
  mounted () {
    this.arr = ['章节', '详情', '评论', '问答', '笔记']
    this.title = 'IOS基础教程之-Camera摄像头'
    this.des = '从实例出发介绍我们的Camera,可以实现Camera的检测，照片录制，图片展示'
    this.arrQuestion = ['本课程适合客户端产品经理，研发人员以及对IOS感兴趣的人群', '（1）数码相机所有相关的API<br/>利用Camera实现相机的各种属性检测']
  }
}
</script>
<style scoped>
    .video{
      position:relative;
      height: 191px;
      width: 375px;
    }
    .video video{
      width: 100%;
      height: 100%
    }
    .video-back{
       position: absolute;
       top: 16px;
       left: 16px;
       text-align:center;
       width: 32px;
       height: 32px;
       line-height: 32px;
       font-size: 18px;
       background: rgba(0,0,0,0.50);
       border-radius: 2px;
       color: #FFFFFF;
     }

     .nav{
       position: relative;
       z-index: 1;
       display: flex;
       width: 375px;
       box-shadow: 0 2px 4px 0 rgba(0,0,0,0.10);
       background: #FFFFFF;
     }
     .nav li{
       flex:1;
       text-align: center;
       height: 44px;
       line-height: 44px;
       font-family: PingFangSC-Regular;
       font-size: 14px;
       color: #2B333B;
     }
     .title{
      height:132px;
      width:375px;
      background: #FFFFFF;
      position:relative;
      text-align:center;
      box-shadow: 0 4px 0 0 rgba(0,0,0,0.10);
     }
     .title h1{
      padding-top:24px;
      padding-left:20px;
      font-family: PingFangSC-Regular;
      font-size: 16px;
      color: #2B333B;
      letter-spacing: 0;
      line-height: 18px;
     }
     .title p{
          padding-top:16px;
          padding-left:20px;
          font-family: PingFangSC-Regular;
          font-family: PingFangSC-Regular;
          font-size: 14px;
          color: #71777D;
          letter-spacing: 0;
          height:40px;
     }
    .question{
      height:240px;
      width:375px;
      position:relative;
      box-shadow: 0 8px 0 0 rgba(0,0,0,0.10);
     }

     ul h1{
      font-family: PingFangSC-Regular;
      font-size: 14px;
      color: #2B333B;
      letter-spacing: 0;
      line-height: 16px;
      margin-top:20px;
      margin-left: 20px;
      width: 305px;
     }

     ul p{
      margin-top:20px;
      margin-left:50px;
      font-family: PingFangSC-Regular;
      font-size: 14px;
      color: #71777D;
      letter-spacing: 0;
      line-height: 20px;
      width: 305px;

     }
     footer{
      background: #FFFFFF;
      width:375px;
      height:26px;

     }

</style>
