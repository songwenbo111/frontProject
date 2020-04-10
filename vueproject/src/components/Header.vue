<template>
  <div class="c-header">
    <ul class="header-ul">
      <li>推荐</li>
      <li>课程</li>
      <li>实战</li>
      <li>职业路线</li>
      <li class="header-search"><img src="../assets/search.png"/>
      </li>
      <li class="header-history"><img src="../assets/history.png"/>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'Header'
}
</script>
<style scope>
  .c-header{
    position:fixed;
    z-index:3;
    width:375px;
    height:44px;
    top:0;
    bottom: 0px;
    left: 0px;
    right: 0px;
    margin-top: 0;
    margin-bottom:auto;
    margin-left:auto;
    margin-right:auto;
    background: #FFF;
    box-shadow: 0 2px 0px 0 rgba(0,0,0,0.10);
  }
  .header-ul li{
    display:inline-block;
    font-size: 16px;
    color: #71777D;
    padding-left:19px;
    height:44px;
    line-height:44px;
  }
  .header-ul img{
    width:17px;
  }
  .header-ul .header-search {
    padding-left: 54px;
    width:18px;
  }
  .header-ul .header-history{
    margin-left: -10px;
  }

</style>
