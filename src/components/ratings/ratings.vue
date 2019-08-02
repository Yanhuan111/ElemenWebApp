<template>
  <div class="container">
    <div class="container-left">
      <div class="score">{{seller.score}}</div>
      <div class="grade">综合评分</div>
      <div class="evaluate">高于周边商家{{seller.rankRate}}%</div>
    </div>
    <div class="container-right">
      <div class="server_wrapper">
        <div class="server">服务态度</div>
        <div class="server_score">{{seller.serviceScore}}</div>
      </div>

      <div class="score_wrapper">
        <div class="goods_score">商品评分</div>
        <div class="goods_grade">{{seller.foodScore}}</div>
      </div>

      <div class="time_wrapper">
        <div class="time">送达时间</div>
        <div class="sum_time">{{seller.deliveryTime}}分钟</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
 name:'ratings',
 props: {
      seller: {
        type: Object
      }
    },
  data() {
    return {};
  }
};
</script>

<style scoped>
.container {
  width: 100%;
  height: 120px;
  border-bottom: 1px solid #dbdbdc;
}
.container-left {
  position: relative;
  width: 130px;
  height: 85px;
  left: 15px;
  top: 20px;
  text-align: center;
  border-right: 1px solid #e1e1e1;
}
.score {
  position: relative;
  top: 10px;
  font-size: 30px;
  color: #fd910e;
}
.grade {
  position: relative;
  top: 15px;
  font-size: 15px;
  font-weight: 300;
}
.evaluate {
  position: relative;
  top: 20px;
  font-size: 12px;
  color: #aeb1b3;
}
.container-right {
  position: relative;
  left: 170px;
  width: 225px;
  height: 85px;
  right: 15px;
  top: -65px;
}
.server_wrapper{
  position: relative;
  top: 15px;
  width: 220px;
  height: 15px;
}
.server {
  color: #42494e;
  font-size: 15px;
}
.server_score{
  position: relative;
  top: -15px;
  color: #fd910e;
  float: right;
}
.score_wrapper{
  position: relative;
  top: 25px;
  width: 220px;
  height: 15px;
}
.goods_score {
  color: #42494e;
  font-size: 15px;
}
.goods_grade{
  position: relative;
  top: -15px;
  left: 22px;
  color: #fd910e;
  float: right;
}
.time_wrapper {
  position: relative;
  top: 35px;
  width: 220px;
  height: 15px;
}
.time {
  top: 35px;
  color: #42494e;
  font-size: 15px;
}
.sum_time {
  position: relative;
  left: 70px;
  top: -13px;
  font-size: 15px;
  font-weight: 500;
  color: #8e9193;
}
</style>

