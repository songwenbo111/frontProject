<template>
  <div class="home-page">
    <v-header></v-header>
    <ul class="nav">
      <li v-for="(item,index) in arrList" :key="index">
        <img :src="item.imgUrl" />
        <span>{{item.name}}</span>
      </li>
    </ul>
    <v-course :arrList="array"></v-course>
    <v-footer></v-footer>
  </div>
</template>
<script>
import Header from '@/components/Header'
import WebImg from '@/assets/web.png'
import WebService from '@/assets/webservice.png'
import Move from '@/assets/move.png'
import Data from '@/assets/data.png'
import BigData from '@/assets/bigdata.png'
import course1 from '@/assets/course1.png'
import course2 from '@/assets/course2.png'
import course3 from '@/assets/course3.png'
import course4 from '@/assets/course4.png'
import course from '@/course/'
import footer from '@/components/footer/'
export default{
  data () {
    return {
      arrList: []
    }
  },
  mounted () {
    this.arrList = [{
      imgUrl: WebImg,
      name: '前端开发'
    }, {
      imgUrl: WebService,
      name: '后端开发'
    }, {
      imgUrl: Move,
      name: '移动开发'
    }, {
      imgUrl: Data,
      name: '数据库'
    }, {
      imgUrl: BigData,
      name: '大数据'
    }]

    this.array = [{
      imgUrl: course1,
      title: '实例妙解Sad和Awk的秘密',
      msg: '中级 ，330在学'
    }, {
      imgUrl: course2,
      title: '实例妙解Sad和Awk的秘密',
      msg: '中级 ，330在学'}, {
      imgUrl: course3,
      title: '实例妙解Sad和Awk的秘密',
      msg: '中级 ，330在学'}, {
      imgUrl: course4,
      title: '实例妙解Sad和Awk的秘密',
      msg: '中级 ，330在学'
    }]
  },
  components: {
    'v-header': Header,
    'v-course': course,
    'v-footer': footer
  }
}
</script>
<style scope>
  .home-page .nav{
    height: 100px;
    padding-top:44px;
    background: #F3F5F7;
    overflow-x: scroll;
    white-space:nowrap;
    font-size:0;
    width:375px;
    margin:auto;

  }
   .nav li{
    width:88px;
    display:inline-block;
    text-align:center;
    font-size:14px;
  }
  .nav li img{
    display: block;
    width:32px;
    height:32px;
    margin: 20px auto 12px;
  }

</style>
