<template>
  <div class="echRight">
    <h3>Vue+Echarts 数据交互Demo(模仿百度图说)</h3>
    <div class="echRight-box">
      <Echarts  :options="chartOption" class="echart"></Echarts>
    </div>
  </div>
</template>

<script>
  import $ from 'jquery';
  import Echarts from 'vue-echarts';
  export default {
    name: 'EchRight',
    components:{
      Echarts,
    },
    data() {
      return {
        chartOption:{
          title: {
            text: "未来一周气温变化",
            subtext: "纯属虚构"
          },
          tooltip: {
            trigger: "axis"
          },
          legend: {
            data: ["最高气温", "最低气温"]
          },
          toolbox: {
            show: true,
            feature: {
              mark: {
                show: true
              },
              dataView: {
                show: true,
                readOnly: true
              },
              magicType: {
                show: false,
                type: ["line", "bar"]
              },
              restore: {
                show: true
              },
              saveAsImage: {
                show: true
              }
            }
          },
          calculable: true,
          xAxis: [
            {
              type: "category",
              boundaryGap: false,
              data: ["周一", "周二", "周三", "周四", "周五", "周六", "周日"]
            }
          ],
          yAxis: [
            {
              type: "value",
              name: "°C"
            }
          ],
          series: [
            {
              name: "最高气温",
              type: "line",
              data: [11, 11, 15, 13, 12, 13, 10],
              center : ['55%', '50%'],
            },
            {
              name: "最低气温",
              type: "line",
              data: [1, -2, 2, 5, 3, 2, 0],
              center : ['55%', '50%'],
            },
          ]
        }
      }
    }
  }
</script>


<style scoped>
/*右侧: Echarts*/
.echRight{
  float:left;
  width:65%;
  height:800px;
  background: #4C4E59;
  border-radius: 4px;
}
.echRight h3{
  color: #f0f0f0;
}
  .echart{
    /*width:550px;*/
    /*height:300px;*/
    margin:0 auto;
    background: #fff !important;
    border-radius: 3px;
    border: 2px solid #ccc;
    outline: 1px solid rgba(188, 188, 188, 0.5);
    box-shadow: rgba(188, 188, 188, 0.5) 1px 1px 1px;
  }
  .echRight-box{
    width: 650px;
    height: 670px;
    padding-top:50px;
    background: #fff;
    margin:0 auto;
  }
</style>
