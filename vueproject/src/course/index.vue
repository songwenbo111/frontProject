<template>
   <ul class="c-course">
      <router-link to="/detail">
       <li v-for="(item,index) in arrList" :key="index">
            <img :src="item.imgUrl">
            <h1>{{item.title}}</h1>
            <p>{{item.msg}}</p>
       </li>
       </router-link>
   </ul>
</template>
<script>
export default {
  props: {
    arrList: Array
  }
}
</script>
<style scoped>
   .c-course{
      padding-top:24px;
   }
   .c-course li{
      position: relative;
      width: 335px;
      height: 72px;
      margin: 0 auto 24px;
   }
   .c-course li img{
      position: absolute;
      width: 108px;
      border-radius: 5px;
      padding-left:20px;
   }
   .c-course li h1{
      padding-left:144px;
      font-family: PingFangSC-Regular;
      font-size: 15px;
      color: #2B333B;
      letter-spacing: 0;
      line-height: 17px;
   }
   .c-course li p{
      font-family: PingFangSC-Light;
      font-size: 12px;
      color: #71777D;
      line-height: 14px;
      margin-top: 8px;
      padding-left: 144px;
   }

</style>
