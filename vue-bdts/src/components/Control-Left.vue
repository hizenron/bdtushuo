<template>
  <div class="control-left">
    <ul class="tab">
      <li class="cur">基础</li>
      <li>标题</li>
      <li>视区</li>
      <li>X轴</li>
      <li>Y轴</li>
      <li>图例</li>
      <li>工具</li>
    </ul>
    <div class="ctr-base active">
      <div class="secNavigation"></div>
    </div>
    <div class="ctr-title">
      <div class="secNavigation"></div>
      <div class="navContent">
        <label>
          <input type="checkbox">
          主标题文本
          <input type="text">
        </label>
        <label>
          <input type="checkbox">
          主标题文本超链接
          <input type="text">
        </label>
        <label>
          <input type="checkbox">
          副标题文本
          <input type="text">
        </label>
        <label>
          <input type="checkbox">
          副标题文本超链接
          <input type="text">
        </label>
      </div>
    </div>
    <div class="ctr-view">
      <div class="secNavigation"></div>
    </div>
    <div class="ctr-xAxis">
      <div class="secNavigation"></div>
    </div>
    <div class="ctr-yAxis">
      <div class="secNavigation"></div>
    </div>
    <div class="ctr-lengend">
      <div class="secNavigation"></div>
    </div>
    <div class="ctr-tooltip">
      <div class="secNavigation"></div>
    </div>
  </div>
</template>

<script>
  import $ from 'jquery';
  export default {
    name: 'CtrLeft',
    data() {
      return {}
    }
  }
  //主题导航点击显示内容
  $(document).ready(function(){
    $(".tab li").click(function(){
      $(".tab li").eq($(this).index()).addClass("cur").siblings().removeClass('cur');
     let i=$(this).index();
      $(".control-left div").eq(i+1).addClass("active").siblings().removeClass("active");
      console.log(i);
    });
  });
</script>


<style scoped>
  /*导航主题*/
.control-left{
  width: 35%;
  float:left;
  color: #f0f0f0;
  overflow: hidden;
}
.control-left ul{
  width: 54px;
  height:800px;
  list-style:none;
  float:left;
  margin:0;
  padding:0;
  background:#373941;
}
.control-left ul li{
  height:36px;
  line-height: 36px;
  display: block;
  color: #f0f0f0;
  font-size: 14px;
  margin:22px 0;
  border-top-left-radius: 4px;
  border-bottom-left-radius: 4px;
  transition: all .3s;
}
  .control-left ul li:hover{
    cursor: pointer;
    background:#5B5D6B;
  }
/*导航显示内容内容*/
  .control-left>div{
    width:600px;
    height: 800px;
    background: #4C4E59;
    float:left;
    text-align: center;
    border-radius: 4px;
  }
  .control-left ul li.cur{
    background: #5B5D6B;
  }
 .control-left>div{
    display: none;
  }
  .control-left div.active{display:block;}
  /*二级导航*/
  .control-left>div div.secNavigation{
    width: 60px;
    height: 800px;
    background: #5B5D6B;
    float: left;
  }
  .control-left>div div.navContent{
    width: 540px;
    height: 800px;
    float: left;
  }
  .control-left>div div.navContent label{
    display: block;
    width:500px;
    float:left;
    text-align: left;
    padding-left:10px;
    margin-top:40px;
  }
  .control-left>div div.navContent label input:nth-child(2) {
    display: inline-block;
    float:right;
    height: 30px;
    line-height: 30px;
    background: transparent;
    border-radius: 5px;
    border: 1px solid #ccc;
  }
</style>
