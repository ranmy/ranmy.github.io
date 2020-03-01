<template>
  <el-carousel :interval="4000" type="card" height="400px">
    <el-carousel-item v-for="item in image_array" :key="item">
      <div>
        <img v-bind:src = "item">
      </div>
    </el-carousel-item>
  </el-carousel>
</template>

<script>
  import head1 from '@/images/head1.jpeg';
  import head2 from '@/images/head2.jpeg';
  import head3 from '@/images/head3.jpeg';
  export default {
    data() {
      return {
        image_array:[head1,head2,head3]
      }
    },
  }
</script>
<style>
  .el-carousel__item h3 {
    color: #475669;
    font-size: 20px;
    opacity: 0.75;
    line-height: 400px;
    margin: 0;
  }
  
  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }
  
  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }
  img {
    max-width: 100%;
    max-height: 100%;
  }
  .div-center{
      margin: 0 auto;
  }
</style>