<template>
  <div class="header">
    <img src="../assets/images/logo.png" alt="">
    <ul>
      <li><a href="#">我的作品</a></li>
      <li><a href="#">添加</a></li>
      <li><a href="#">保存</a></li>
      <li><a href="#">页面设计</a></li>
      <li><a href="#">分享</a></li>
      <li><a href="#">预览</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
    }
  }
}
</script>


<style scoped>
.header{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1004;
  background: #373941;
  height: 44px;
  font-size:14px;
  color: #f0f0f0;
  -webkit-box-shadow: rgba(0, 0, 0, 0.4) 0px 1px 1px;
  -moz-box-shadow: rgba(0, 0, 0, 0.4) 0px 1px 1px;
  box-shadow: rgba(0, 0, 0, 0.5) 0px 1px 1px;
}
.header img{
  float:left;
  width: 110px;
  margin-left:20px;
}
.header ul{
  list-style: none;
}
.header ul li{
  display: inline-block;
  float: left;
  margin-left: 35px;
}
.header ul li a{
  font-size: 14px;
  color: #f0f0f0;
  text-decoration: none;
}
.header ul li a:hover,.header ul li a:active{
  color: #ccc;
}

</style>
