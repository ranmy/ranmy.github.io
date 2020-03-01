<template>
    <div style="width: 100%;">
      <el-card :body-style="{ padding: '0px' }">
      <div style="padding: 14px;">
        <span>{{ text }}</span>
      </div>
      <video v-if="isVideo" :src="src" controls="controls"></video>
      <img v-else :src="src"/>
    </el-card>
    </div>
    
</template>
<style>
  .time {
    font-size: 13px;
    color: #999;
  }
  
  .bottom {
    margin-top: 13px;
    line-height: 12px;
  }

  .button {
    padding: 0;
    float: right;
  }
  img {
    max-width: 100%;
    max-height: 100%;
  }

  .clearfix:before,
  .clearfix:after {
      display: table;
      content: "";
  }
  
  .clearfix:after {
      clear: both
  }
</style>

<script>
export default {
  props:[
    'src',
    "isVideo",
    'text'
  ],
  data() {
    return {
      currentDate: new Date()
    };
  }
}
</script>