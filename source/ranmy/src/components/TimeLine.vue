<template>
<div class="block time-cotext">
  <el-timeline v-for = "item in timeItem" :key="item">

    <el-timeline-item v-bind:timestamp="item.timestamp" v-bind:placement="item.placement">
      <TimeCardItem :text = "item.text" :src="item.src" :isVideo="item.isVideo"/>
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
            "src":require("./../video/20200202-1.mp4"),
            "isVideo":true,
            "text":"宝宝出生了！迷茫的小眼神！"
          },
          {
            "timestamp":"2020/02/02",
            "placement":"top",
            "src":require("./../images/head1.jpeg"),
            "isVideo":false,
            "text":"宝宝出生了！迷茫的小眼神！"
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
  width: 80%;
  margin: 0 auto;
}
</style>