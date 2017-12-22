<template>
  <div class="index">
    <Header></Header>
    <CtrLeft></CtrLeft>
    <EchLeft></EchLeft>
  </div>
</template>

<script>
import Header from '../components/Header.vue';
import CtrLeft from '../components/Control-Left.vue';
import EchLeft from '../components/Echarts-right.vue';
  export default {
    components:{
      Header,
      CtrLeft,
      EchLeft
    },
    data () {
      return {
      }
    }
  }
</script>


<style scoped>
div.index{
  width:100%;
  margin:0;
  padding:0;
  overflow: hidden;
}

</style>
