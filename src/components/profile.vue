<<<<<<< HEAD
<template>
  <div class="info">
    <h1>作品集</h1>
    <transition
      :duration="{ enter: 2500, leave: 1500 }"
      enter-active-class="animated fadeInRight">
      <div class="cont"  v-if="show">
        <el-row :gutter="20">
          <template v-for="item in profiles">
            <el-col :key="item.name" :span="12" :xs="24">
              <div class="item">
                <h2 v-text="item.name"></h2>
                <p v-text="'技术栈: ' + item.skills"></p>
                <p v-text="item.content"></p>
                <p v-text="'github地址: ' + item.github"></p>
              </div>
            </el-col>
          </template>
        </el-row>
      </div>
    </transition>
  </div>
</template>
<script>
export default {
  data () {
    return {
      show: false,
      profiles: [
        {
          name: '悦动后台管理系统（yuedong-admin）',
          skills: 'NodeJS express MD5 router mysql 连接池 Promise socket.io vue vue-router axios element-ui qs vue-cropper',
          content: '这是悦动项目的服务端，基于NodeJS使用express框架，数据库为mysql，使用express-promise-router统一捕获error，开发中用到git、vscode工具这个代理商城项目有完整的前后端页面，功能也完全响应悦动客户端.后端页面也完全实现了网站整体设置，用户统计，活动统计，管理员管理、用户管理、活动管理、话题管理、场馆管理等功能！',
          github: 'https://github.com/GuoLiBin6/yuedong-admin'
        },
        {
          name: '悦动后台管理系统（yuedong-admin）',
          skills: 'NodeJS express MD5 router mysql 连接池 Promise socket.io vue vue-router axios element-ui qs vue-cropper',
          content: '这是悦动项目的服务端，基于NodeJS使用express框架，数据库为mysql，使用express-promise-router统一捕获error，开发中用到git、vscode工具这个代理商城项目有完整的前后端页面，功能也完全响应悦动客户端.后端页面也完全实现了网站整体设置，用户统计，活动统计，管理员管理、用户管理、活动管理、话题管理、场馆管理等功能！',
          github: 'https://github.com/GuoLiBin6/yuedong-admin'
        },
        {
          name: '购物APP（Go）',
          skills: 'jQueryMobile BootStrap jquery-event webstroage AJAX url json',
          content: '这个商城项目具有完整的前端页面和后端数据接口，实现了商城的部分功能，用户登录注册，状态管理，商品分类展示搜索，热销商品推荐，商品详情展示，加入购物车、查看购物车!',
          github: 'https://github.com/GuoLiBin6/first-app'
        },
        {
          name: '资芽（ziya）',
          skills: 'ionic rem',
          content: '这是一个信息咨询类Android APP，是学习ionic过程中制作的，完成登录、注册、优质信息服务推荐、信息发布、聊天、设置等页面的编写，虽然只有前端页面，但是使我很好的理解了前端组件化开发和MVC模式！',
          github: 'https://github.com/GuoLiBin6/ziya'
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
  color: whitesmoke;
}
.cont{
  margin: 20px auto;
  width: 90%;
  border-radius: 15px;
}
.item {
    background-color: rgba(0, 0, 0, 0.2);
    padding: 10px;
    border-radius: 15px;
    margin: 10px auto;
}
.item:hover {
        border-radius: 25px;
        background-color: rgba(10, 135, 87, 0.2);
      }
       p {
           margin-top: 10px;
        text-align: left;
        text-indent: 28px;
        font-size: 18px;
        line-height: 20px;
      
      }
</style>
=======
<template>
  <div class="info">
    <h1>作品集</h1>
    <transition
      :duration="{ enter: 2500, leave: 1500 }"
      enter-active-class="animated fadeInRight">
      <div class="cont"  v-if="show">
        <el-row :gutter="20">
          <template v-for="item in profiles">
            <el-col :key="item.name" :span="12" :xs="24">
              <div class="item">
                <h2 v-text="item.name"></h2>
                <p v-text="'技术栈: ' + item.skills"></p>
                <p v-text="item.content"></p>
                <p v-text="'github地址: ' + item.github"></p>
              </div>
            </el-col>
          </template>
        </el-row>
      </div>
    </transition>
  </div>
</template>
<script>
export default {
  data () {
    return {
      show: false,
      profiles: [
        {
          name: '悦动后台管理系统（yuedong-admin）',
          skills: 'NodeJS express MD5 router mysql 连接池 Promise socket.io vue vue-router axios element-ui qs vue-cropper',
          content: '这是悦动项目的服务端，基于NodeJS使用express框架，数据库为mysql，使用express-promise-router统一捕获error，开发中用到git、vscode工具这个代理商城项目有完整的前后端页面，功能也完全响应悦动客户端.后端页面也完全实现了网站整体设置，用户统计，活动统计，管理员管理、用户管理、活动管理、话题管理、场馆管理等功能！',
          github: 'https://github.com/GuoLiBin6/yuedong-admin'
        },
        {
          name: '悦动后台管理系统（yuedong-admin）',
          skills: 'NodeJS express MD5 router mysql 连接池 Promise socket.io vue vue-router axios element-ui qs vue-cropper',
          content: '这是悦动项目的服务端，基于NodeJS使用express框架，数据库为mysql，使用express-promise-router统一捕获error，开发中用到git、vscode工具这个代理商城项目有完整的前后端页面，功能也完全响应悦动客户端.后端页面也完全实现了网站整体设置，用户统计，活动统计，管理员管理、用户管理、活动管理、话题管理、场馆管理等功能！',
          github: 'https://github.com/GuoLiBin6/yuedong-admin'
        },
        {
          name: '购物APP（Go）',
          skills: 'jQueryMobile BootStrap jquery-event webstroage AJAX url json',
          content: '这个商城项目具有完整的前端页面和后端数据接口，实现了商城的部分功能，用户登录注册，状态管理，商品分类展示搜索，热销商品推荐，商品详情展示，加入购物车、查看购物车!',
          github: 'https://github.com/GuoLiBin6/first-app'
        },
        {
          name: '资芽（ziya）',
          skills: 'ionic rem',
          content: '这是一个信息咨询类Android APP，是学习ionic过程中制作的，完成登录、注册、优质信息服务推荐、信息发布、聊天、设置等页面的编写，虽然只有前端页面，但是使我很好的理解了前端组件化开发和MVC模式！',
          github: 'https://github.com/GuoLiBin6/ziya'
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
  color: whitesmoke;
}
.cont{
  margin: 20px auto;
  width: 90%;
  border-radius: 15px;
}
.item {
    background-color: rgba(0, 0, 0, 0.2);
    padding: 10px;
    border-radius: 15px;
    margin: 10px auto;
}
.item:hover {
        border-radius: 25px;
        background-color: rgba(10, 135, 87, 0.2);
      }
       p {
           margin-top: 10px;
        text-align: left;
        text-indent: 28px;
        font-size: 18px;
        line-height: 20px;
      
      }
</style>
>>>>>>> 修改配置文件后打包
