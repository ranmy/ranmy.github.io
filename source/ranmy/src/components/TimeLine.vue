<template>
<div class="block time-cotext">
  <el-timeline v-for = "item in timeItem" :key="item">

    <el-timeline-item v-bind:timestamp="item.timestamp" 
    v-bind:placement="item.placement" size = "large" icon="el-icon-star-off"
    color="#0bbd87">
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
            "text":"我是谁？我在哪？我在干什么？"
          },
          {
            "timestamp":"2020/02/03",
            "placement":"top",
            "src":require("./../video/20200203-1.mp4"),
            "isVideo":true,
            "text":"谁开的灯啊，还让不让人睡觉啦~~~"
          },
          {
            "timestamp":"2020/02/07",
            "placement":"top",
            "src":require("./../video/20200207-1.mp4"),
            "isVideo":true,
            "text":"又来！能不能等我睡醒？！"
          },
          {
            "timestamp":"2020/02/07",
            "placement":"top",
            "src":require("./../video/20200207-2.mp4"),
            "isVideo":true,
            "text":"嗯，这段能不能删掉？！！！"
          },
          {
            "timestamp":"2020/02/07",
            "placement":"top",
            "src":require("./../video/20200207-3.mp4"),
            "isVideo":true,
            "text":"嗯？是不是该吃晚饭了。"
          },
          {
            "timestamp":"2020/02/08",
            "placement":"top",
            "src":require("./../video/20200208-1.mp4"),
            "isVideo":true,
            "text":"天亮了么？我还没睡醒呢。"
          },
          {
            "timestamp":"2020/02/08",
            "placement":"top",
            "src":require("./../video/20200208-2.mp4"),
            "isVideo":true,
            "text":"别闹别闹，我再睡会。"
          },
          {
            "timestamp":"2020/02/09",
            "placement":"top",
            "src":require("./../images/20200209-1.jpeg"),
            "isVideo":false,
            "text":"我说，全家福能不能等我睁开眼？！"
          },
          {
            "timestamp":"2020/02/10",
            "placement":"top",
            "src":require("./../video/20200210-1.mp4"),
            "isVideo":true,
            "text":"手机是不是拿反了？"
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