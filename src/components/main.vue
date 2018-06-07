<template>
  <div class="resume" @mousewheel="mouse" :style="{backgroundImage:`url(${img})`,height: `${clientHeight}`}">
    <!-- 第一部分 -->
    <transition :duration="{ enter: 2500, leave: 1500 }" enter-active-class="animated zoomInDown" leave-active-class="animated zoomOutUp" >
      <div class="section" :style="{height: `${clientHeight}`}" v-if="init === 1">
        <div class="sec">
          <Info></Info>
        </div>
      </div>
    </transition>
    <!-- 第二部分 -->
    <transition :duration="{ enter: 2500, leave: 1500 }" enter-active-class="animated zoomInDown" leave-active-class="animated zoomOutUp">
      <div class="section" :style="{height: `${clientHeight}`}" v-if="init === 2">
        <div class="sec">
            <Skills></Skills>
        </div>
      </div>
    </transition>
    <!-- 第三部分 -->
    <transition :duration="{ enter: 2500, leave: 1500 }" enter-active-class="animated zoomInDown" leave-active-class="animated zoomOutUp">
      <div class="section" :style="{height: `${clientHeight}`}" v-if="init === 3">
        <div class="sec">
            <Profile></Profile>  
        </div>
      </div>
    </transition>
    <!-- 第四部分 -->
    <transition :duration="{ enter: 2500, leave: 1500 }" leave-active-class="animated zoomOutUp" enter-active-class="animated zoomInDown">
      <div class="section" :style="{height: `${clientHeight}`}" v-if="init === 4">
        <div class="sec">
            <Concat></Concat>
        </div>
      </div>
    </transition>
    <div class="next"><i class="iconfont icon-arrow-down setarrow" @click="nextPage"></i></div>
    <div class="time">更改时间：2018-6-7</div>
  </div>
</template>

<script>
import animate from 'animate.css';
import $ from 'jquery';
import Info from './info';
import Skills from './skills';
import Profile from './profile';
import Concat from './concat';
export default {
  name: 'Main',
  components:{
    Info,
    Skills,
    Profile,
    Concat
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      init:1,
      img: require('../assets/banner.jpg'),
      clientHeight:'900px',
      lastscroll:0
    }
  },
  methods:{
    mouse (event) {
      // 防止用户短时间内滚动多次，设置滚动间隔大于一秒才能生效
      // 判断滚动间隔时间
      let scrollduration = event.timeStamp - this.lastscroll
      if (scrollduration > 1000) {
        // 将这一次的滚动时间记录为上一次合法的滚动时间
        this.lastscroll = event.timeStamp
        // 判断滚动方向进行操作
        if (event.deltaY > 0) {
          if (this.init === 4) {
            this.init = 1
          } else {
            this.init = this.init + 1
          }
        } else {
          if (this.init === 1) {
            this.init = 4
          } else {
            this.init = this.init - 1
          }
        }
      } else {
        // 如果滚动不合法就不做任何操作
      }
    },
    nextPage () {
      if (this.init === 4) {
        this.init = 1
      } else {
        this.init = this.init + 1
      }
    }
  },
  //设置屏幕高度
  mounted(){
    this.clientHeight = `${document.documentElement.clientHeight}px`;
    window.onresize = () => {
      this.clientHeight = `${document.documentElement.clientHeight}px`
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.resume{
  background-repeat:no-repeat;
  background-position: center center;
  background-size:100% 100%;
  -moz-background-size:100% 100%;
  overflow: hidden;
  
  /* background-image: url(../assets/banner.jpg); */
}
.section{
   width: 100%;
   background:rgba(0,0,0,0.3);
   position: fixed;
   left: 0;
   top: 0;
  }
  .sec{
    width: 100%;
  }
  
  @keyframes myfirst {
  0%, 20%, 50%, 80%, 100% {
    -moz-transform: translateY(0);
    -ms-transform: translateY(0);
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }
  40% {
    -moz-transform: translateY(-30px);
    -ms-transform: translateY(-30px);
    -webkit-transform: translateY(-30px);
    transform: translateY(-30px);
  }
  60% {
    -moz-transform: translateY(-15px);
    -ms-transform: translateY(-15px);
    -webkit-transform: translateY(-15px);
    transform: translateY(-15px);
  }
}
  .setarrow{
    font-size: 50px;
    color: rgba(255, 255, 255, 0.5);
    position: fixed;
    left: 48%;
    bottom: 20px;
    animation: myfirst 3s infinite;  
  }
  .time{
    position: fixed;
    right: 20px;
    bottom: 20px;
    color:rgba(100, 157, 255,.5);
  }
</style>
