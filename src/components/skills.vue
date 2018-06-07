<<<<<<< HEAD
<template>
  <div class="info">
    <h1>技能</h1>
    <transition
      :duration="{ enter: 2500, leave: 1500 }"
      leave-active-class="animated fadeOutRight"
      enter-active-class="animated fadeInLeft">
      <div class="cont"  v-if="show">
        <template v-for="skill in skills">
          <el-row :gutter="20" :key="skill.name">
            <el-col :span="6">
              <div class="left" :style="{backgroundColor: `${skill.background}`}">
                <h2>{{skill.name}}</h2>
              </div>
            </el-col>
          <el-col :span="18">
              <el-row :gutter="10">
                <template v-for="child in skill.child">
                  <el-col :span="6"  :key="child.name">
                    <div class="right" :style="{backgroundColor: child.background}">
                      <h3>{{child.name}}</h3>
                    </div>
                  </el-col>
                </template>
              </el-row>
          </el-col>
        </el-row>
        </template>
      </div>
    </transition>
  </div>
</template>
<script>
export default {
  data () {
    return {
      show: false,
      skills: [
        {
          name: '前端',
          background: 'rgba(29, 218, 61, 0.2)',
          child: [
            {name: 'HTML5', background: 'rgba(29, 218, 61, 0.2)'},
            {name: 'CSS3', background: 'rgba(29, 218, 61, 0.2)'},
            {name: 'Ajax', background: 'rgba(29, 218, 61, 0.2)'},
            {name: 'SPA', background: 'rgba(29, 218, 61, 0.2)'},
            {name: 'Vue', background: 'rgba(29, 218, 61, 0.2)'},
            {name: 'AngularJS', background: 'rgba(29, 218, 61, 0.2)'},
            {name: 'Ionic', background: 'rgba(29, 218, 61, 0.2)'},
            {name: 'Bootstrap', background: 'rgba(29, 218, 61, 0.2)'}
          ]
        },
        {
          name: '服务端',
          background: 'rgba(211, 184, 30, 0.2)',
          child: [
            {name: 'ES6', background: 'rgba(211, 184, 30, 0.2)'},
            {name: 'NodeJs', background: 'rgba(211, 184, 30, 0.2)'},
            {name: 'express', background: 'rgba(211, 184, 30, 0.2)'},
            {name: 'MYSQL', background: 'rgba(211, 184, 30, 0.2)'},
            {name: 'MD5', background: 'rgba(211, 184, 30, 0.2)'},
            
          ]
        },
        {
          name: '工具',
          background: 'rgba(232, 13, 24, 0.2)',
          child: [
            {name: 'Git', background: 'rgba(232, 13, 24, 0.2)'},
            {name: 'WebPack', background: 'rgba(232, 13, 24, 0.2)'},
            {name: 'PS', background: 'rgba(232, 13, 24, 0.2)'},
            {name: 'VS Code', background: 'rgba(232, 13, 24, 0.2)'},
            {name: 'shell', background: 'rgba(232, 13, 24, 0.2)'},
            {name: 'ProcessOn', background: 'rgba(232, 13, 24, 0.2)'},
            {name: '墨刀', background: 'rgba(232, 13, 24, 0.2)'}          
          ]
        }
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

<style scoped>
.info{
  margin: 60px auto;
  color: white;
}
.cont{
  margin: 20px auto;
  width: 60%;
  border-radius: 15px;
}
.left {
    margin: 10px auto;
    width: 100%;
    height: 160px;
    line-height: 160px;
}
.right {
    margin: 10px auto;
    height: 70px;
    line-height: 70px;
}
</style>
=======
<template>
  <div class="info">
    <h1>技能</h1>
    <transition
      :duration="{ enter: 2500, leave: 1500 }"
      leave-active-class="animated fadeOutRight"
      enter-active-class="animated fadeInLeft">
      <div class="cont"  v-if="show">
        <template v-for="skill in skills">
          <el-row :gutter="20" :key="skill.name">
            <el-col :span="6">
              <div class="left" :style="{backgroundColor: `${skill.background}`}">
                <h2>{{skill.name}}</h2>
              </div>
            </el-col>
          <el-col :span="18">
              <el-row :gutter="10">
                <template v-for="child in skill.child">
                  <el-col :span="6"  :key="child.name">
                    <div class="right" :style="{backgroundColor: child.background}">
                      <h3>{{child.name}}</h3>
                    </div>
                  </el-col>
                </template>
              </el-row>
          </el-col>
        </el-row>
        </template>
      </div>
    </transition>
  </div>
</template>
<script>
export default {
  data () {
    return {
      show: false,
      skills: [
        {
          name: '前端',
          background: 'rgba(29, 218, 61, 0.2)',
          child: [
            {name: 'HTML5', background: 'rgba(29, 218, 61, 0.2)'},
            {name: 'CSS3', background: 'rgba(29, 218, 61, 0.2)'},
            {name: 'Ajax', background: 'rgba(29, 218, 61, 0.2)'},
            {name: 'SPA', background: 'rgba(29, 218, 61, 0.2)'},
            {name: 'Vue', background: 'rgba(29, 218, 61, 0.2)'},
            {name: 'AngularJS', background: 'rgba(29, 218, 61, 0.2)'},
            {name: 'Ionic', background: 'rgba(29, 218, 61, 0.2)'},
            {name: 'Bootstrap', background: 'rgba(29, 218, 61, 0.2)'}
          ]
        },
        {
          name: '服务端',
          background: 'rgba(211, 184, 30, 0.2)',
          child: [
            {name: 'ES6', background: 'rgba(211, 184, 30, 0.2)'},
            {name: 'NodeJs', background: 'rgba(211, 184, 30, 0.2)'},
            {name: 'express', background: 'rgba(211, 184, 30, 0.2)'},
            {name: 'MYSQL', background: 'rgba(211, 184, 30, 0.2)'},
            {name: 'MD5', background: 'rgba(211, 184, 30, 0.2)'},
            
          ]
        },
        {
          name: '工具',
          background: 'rgba(232, 13, 24, 0.2)',
          child: [
            {name: 'Git', background: 'rgba(232, 13, 24, 0.2)'},
            {name: 'WebPack', background: 'rgba(232, 13, 24, 0.2)'},
            {name: 'PS', background: 'rgba(232, 13, 24, 0.2)'},
            {name: 'VS Code', background: 'rgba(232, 13, 24, 0.2)'},
            {name: 'shell', background: 'rgba(232, 13, 24, 0.2)'},
            {name: 'ProcessOn', background: 'rgba(232, 13, 24, 0.2)'},
            {name: '墨刀', background: 'rgba(232, 13, 24, 0.2)'}          
          ]
        }
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

<style scoped>
.info{
  margin: 60px auto;
  color: white;
}
.cont{
  margin: 20px auto;
  width: 60%;
  border-radius: 15px;
}
.left {
    margin: 10px auto;
    width: 100%;
    height: 160px;
    line-height: 160px;
}
.right {
    margin: 10px auto;
    height: 70px;
    line-height: 70px;
}
</style>
>>>>>>> 修改配置文件后打包
