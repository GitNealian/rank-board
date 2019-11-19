<template>
  <div>
    <el-card class="card-item" v-for="d in dataList" :key="d" :id="'item'+d">
      <div class="board">
        <div class="first-place-number">{{d}}</div>
        <div class="group-name">NEALIAN</div>
        <div class="score"></div>
        <div class="total-score"></div>
      </div>
      <div class="frosted-glass"></div>
    </el-card>
  </div>
</template>
<style scoped>
</style>
<style>
.first-place-number {
  font-size: 32px;
  color: gold;
  font-family: Broadway BT;
  padding-left: 10px;
  float: left;
}
.group-name {
  font-size: 18px;
  margin-left: 20px;
  padding-top: 10px;
  float: left;
  font-family: ST Gothic Hv;
  color: bisque;
}
.el-card.is-always-shadow:hover {
  box-shadow: 1px 4px 8px 2px #0b0172;
}
.el-card {
  border: none !important;
}
.board {
  position: relative;
  float: left;
  z-index: 1;
  top: 0;
  bottom: 0;
  color: white;
  padding: 10px;
}
.frosted-glass {
  position: relative;
  top: 0;
  bottom: 0;
  height: 60px;
  background: radial-gradient(
    rgba(255, 255, 255, 0.1),
    rgba(255, 255, 255, 0.1)
  );
  background: #0c18b8;
  background-image: radial-gradient(
    rgba(255, 255, 255, 0.1),
    rgba(255, 255, 255, 0.1),
    rgba(255, 255, 255, 0.1),
    rgba(255, 255, 255, 0.1),
    rgba(255, 255, 255, 0.1),
    rgb(5, 33, 230)
  );
  -webkit-filter: blur(5px);
  -moz-filter: blur(5px);
  -ms-filter: blur(5px);
  -o-filter: blur(5px);
  filter: blur(5px);
  filter: progid:DXImageTransform.Microsoft.Blur(PixelRadius=4, MakeShadow=false);
  color: white;
}
body {
  background: lightgray;
}

@keyframes upRank {
  from {
    top: 0;

    box-shadow: 1px 4px 8px 2px #0b0172;
  }
  50% {
    box-shadow: 1px 4px 8px 2px #0b0172;
  }
  to {
    top: -65px;
    box-shadow: none;
  }
}

@keyframes downRank {
  from {
    top: 0;
  }
  to {
    top: 65px;
  }
}
.card-item {
  margin-bottom: 5px;
}
.el-card__body {
  background: #d2d2d6cf;
  padding: 0 !important;
}
#item1 {
  position: relative;
  animation: downRank 1s;
  -moz-animation: downRank 1s; /* Firefox */
  -webkit-animation: downRank 1s; /* Safari 和 Chrome */
  -o-animation: downRank 1s;
  animation-fill-mode: forwards;
}

#item2 {
  position: relative;
  animation: upRank 1s;
  -moz-animation: upRank 1s; /* Firefox */
  -webkit-animation: upRank 1s; /* Safari 和 Chrome */
  -o-animation: upRank 1s;
  animation-fill-mode: forwards;
  z-index: 1;
}
</style>
<script>
export default {
  data() {
    return {
      dataList: [1, 2, 3, 4, 5]
    };
  },
  methods: {
    upRank(id) {
      alert(id);
    }
  }
};
</script>