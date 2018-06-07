<template>
  <div class="info">
    <h1>基本资料</h1>
    <transition :duration="{ enter: 2500, leave: 1500 }" enter-active-class="animated fadeInUp">
      <div class="cont"  v-if="show">
        <img class="avatar" src="../assets/avatar.jpg" alt="">
        <h2>我常面带微笑，因为我热爱这工作</h2>
        <p>我叫郭丽斌</p>
        <p>两年前端学习经验，暂无企业工作经验</p>
        <div class="state">
          <el-row :gutter="30">
            <template v-for="item in states">
              <el-col :span="6" :xs="12" :key="item.icon">
                <div class="iconBox">
                  <i class="iconfont iconSet" :class="item.icon"></i>
                </div>
                <p v-text="item.val"></p>
              </el-col>
            </template>
          </el-row>
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
import animate from 'animate.css';
import $ from 'jquery';

export default {
  data () {
    return {
      show: false,
      states: [
        {icon: 'icon-nianling', val: '年龄/23'},
        {icon: 'icon-xueli', val: '学历/本科'},
        {icon: 'icon-weizhi', val: '坐标/石家庄'},
        {icon: 'icon-zhiwei', val: '状态/找实习'}
      ]
    }
  },
  methods: {
    timeout () {
      setTimeout(() => {
        this.show = true
      }, 1000)
    }
  },
  mounted () {
    this.timeout()
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.info{
  margin: 60px auto;
  color: white;
  /* font-family: '幼圆' */
}
img{
  margin-top: 30px;
  width: 120PX;
  /* height: 120PX; */
  border-radius: 50%;
}
.cont{
  margin: 20px auto;
  width: 60%;
  background-color:rgba(0, 0, 0, 0.5);
  border-radius: 15px;
}
h2{
  margin: 10px 0;
}
p{
  font-size: 18px;
  height: 40px;
  line-height: 40px;

}
.iconBox {
        width: 80px;
        height: 80px;
        border-radius: 40px;
        border: 1px solid rgba(9, 92, 49, .5);
        margin: 5px auto;
        background-color: rgba(13, 73, 87, 0.4);
        /* &:hover {
          background-color: rgba(13, 73, 87, 0.8);
        } */
}
.iconBox:hover{
  background-color: rgba(13, 73, 87, 0.8);
}
.iconSet{
  height: 80px;
  line-height: 80px;
  width: 70px;
  font-size: 50px;
}
.iconSet:hover{
  font-size: 55px;
}
.state{
  padding:20px 0 30px 0;
}
</style>
