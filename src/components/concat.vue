<<<<<<< HEAD
<template>
  <div class="info">
    <h1>联系我</h1>
    <transition
      :duration="{ enter: 2500, leave: 1500 }"
      enter-active-class="animated fadeInDown">
      <div class="cont"  v-if="show">
        <div class="assessment">
          <h2>自我评价</h2>
          <p>高效的自学能力,具备独立分析解决问题能力</p>
          <p>强烈的自我驱动力,只喜欢优雅的代码</p>
          <p>熟悉组件化开发</p>
        </div>
        <div class="honor">
          <h2>兴趣爱好</h2>
          <p>喜欢优秀的网页设计</p>
          <p>喜欢尝试新事物</p>
        </div>
        <div class="contact">
          <h2>联系我</h2>
          <p><i class="iconfont icon-shouji"></i>  15703286327</p>
          <p><i class="iconfont icon-youxiang"></i>  glbin533@163.com</p>
        </div>
      </div>
    </transition>
  </div>
</template>
<script>
export default {
  data () {
    return {
      show: false,
      
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
<style scoped>
.info{
  margin: 60px auto;
  color: white;
}
.cont{
  margin: 20px auto;
  width: 60%;
  border-radius: 15px;
  margin: 20px auto;
     background-color: rgba(117, 100, 150, 0.3);
     border-radius: 25px;
     padding: 30px 0;
}
.acount {
       width: 30%;
       margin: 10px auto;
}
h2{
    margin: 10px auto;
}
p{
    height: 30px;
    line-height: 30px;
}
.iconBox {
         width: 40px;
         height: 40px;
         border-radius: 20px;
         border: 1px solid rgba(9, 92, 49, .5);
         margin: 5px auto;
         background-color: rgba(13, 73, 87, 0.4);
}
 .iconSet {
           font-size: 1.5rem;
           line-height: 40px;
           cursor: pointer;
           color: rgba(220, 228, 220, 0.7);
         }
</style>
=======
<template>
  <div class="info">
    <h1>联系我</h1>
    <transition
      :duration="{ enter: 2500, leave: 1500 }"
      enter-active-class="animated fadeInDown">
      <div class="cont"  v-if="show">
        <div class="assessment">
          <h2>自我评价</h2>
          <p>高效的自学能力,具备独立分析解决问题能力</p>
          <p>强烈的自我驱动力,只喜欢优雅的代码</p>
          <p>熟悉组件化开发</p>
        </div>
        <div class="honor">
          <h2>兴趣爱好</h2>
          <p>喜欢优秀的网页设计</p>
          <p>喜欢尝试新事物</p>
        </div>
        <div class="contact">
          <h2>联系我</h2>
          <p><i class="iconfont icon-shouji"></i>  15703286327</p>
          <p><i class="iconfont icon-youxiang"></i>  glbin533@163.com</p>
        </div>
      </div>
    </transition>
  </div>
</template>
<script>
export default {
  data () {
    return {
      show: false,
      
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
<style scoped>
.info{
  margin: 60px auto;
  color: white;
}
.cont{
  margin: 20px auto;
  width: 60%;
  border-radius: 15px;
  margin: 20px auto;
     background-color: rgba(117, 100, 150, 0.3);
     border-radius: 25px;
     padding: 30px 0;
}
.acount {
       width: 30%;
       margin: 10px auto;
}
h2{
    margin: 10px auto;
}
p{
    height: 30px;
    line-height: 30px;
}
.iconBox {
         width: 40px;
         height: 40px;
         border-radius: 20px;
         border: 1px solid rgba(9, 92, 49, .5);
         margin: 5px auto;
         background-color: rgba(13, 73, 87, 0.4);
}
 .iconSet {
           font-size: 1.5rem;
           line-height: 40px;
           cursor: pointer;
           color: rgba(220, 228, 220, 0.7);
         }
</style>
>>>>>>> 修改配置文件后打包
