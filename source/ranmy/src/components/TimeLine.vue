<template>
<div class="block time-cotext">
  <el-timeline v-for = "item in timeItem" :key="item">

    <el-timeline-item v-bind:timestamp="item.timestamp" v-bind:placement="item.placement">
      <TimeCardItem/>
    </el-timeline-item>
  
  </el-timeline>
</div>
</template>

<script type="text/javascript">
  import TimeCardItem from './TimeCardItem.vue'
  export default {
    data() {
      return {
        timeItem:[
          {
            "timestamp":"2020/02/02",
            "placement":"top",
            "image-url":"@/images/haed1.jpeg",
            "text-context":"aaaaaaaaaaaaaaa啊啊啊啊啊啊啊  啊啊啊啊啊啊"
          }
        ]
      }
    },
    components:{
      TimeCardItem
    }
  }
</script>
<style type="text/css">
.time-cotext{
  width: 75%;
  margin: 0 auto;
}
</style>