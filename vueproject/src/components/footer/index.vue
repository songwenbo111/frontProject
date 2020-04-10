<template>
    <div class="c-footer">
       <ul class="footer-ul">
          <li>
             <img src="../../assets/home.png">
             <span>首页</span>
          </li>
          <li>
             <img src="../../assets/see.png">
             <span>发现</span>
          </li>
          <li>
             <img src="../../assets/download.png">
             <span>下载</span>
          </li>
          <li>
             <img src="../../assets/me.png">
             <span>我的</span>
          </li>

       </ul>
    </div>
</template>
<script>
export default {
  name: 'footer'
}
</script>
<style scoped>
  .c-footer{
    position: fixed;
    z-index: 3;
    top:545px;
    width: 375px;
    opacity: 0.9;
    background: #FFFFFF;
    bottom: 0px;
    left: 0px;
    right: 0px;
    margin-top: auto;
    margin-bottom:auto;
    margin-left:auto;
    margin-right:auto;
  }
  .footer-ul{
     display:flex;
  }
  .footer-ul li{
     display: flex;
     flex-direction: column;
     height: 50px;
     padding-left:35px;
     padding-right:35px;
     align-items: center;
     justify-content: center;
     font-size: 10px;
     color: #2B333B;
  }
  .footer-ul li img{
     padding-top:8px;
     padding-bottom:4px;
     width: 24px;
  }
</style>
