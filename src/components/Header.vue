<template>
  <!-- <v-app-bar :elevation="2" scroll-behavior="hide">
    <template v-slot:image>
          <v-img
            src="@/assets/logo-gray.png"
            max-width="10%"
          ></v-img>
      </template>

    <v-app-bar-title style="margin-left: 10%;">成都小五郎企业管理有限公司</v-app-bar-title>

    <template v-slot:append>

      <v-btn @click="show_wechat" icon="mdi-wechat"></v-btn>
      <v-btn><svg-icon type="mdi" :path="phone_path"></svg-icon>>: 15882820920</v-btn>
    </template>
  </v-app-bar> -->
  <div class="header">
    <div class="container headers">
    <div class="logo fl">
    <a href="/" title="昆明清友商务调查有限公司">
        <img src="http://img01.fuhai360.com/kmqy/202212/202212141059337455.jpg" alt="昆明清友商务调查有限公司"></a>
    </div>
      <div class="navs">
                    <b></b>
                    <b></b>
                    <b></b>
                    </div>
            <div class="nav fl">
                
                                              <div class="nav_button"></div>
                        
                                          <ul><li><a href="/">网站首页</a></li><li><a href="/product-1005.html">服务范围</a><ul><li><a href="/fwdx.html">服务对象</a></li></ul></li><li><a href="/article.html">新闻中心</a><ul><li><a href="/article-1001.html">法律法规</a></li><li><a href="/article-1002.html">调查知识</a></li><li><a href="/article-1004.html">个案分析</a></li></ul></li><li><a href="/bmyd.html">保密约定</a></li><li><a href="/sfbz.html">收费标准</a></li><li><a href="/about.html" class="cur">关于清友</a></li><li><a href="/contact.html">联系我们</a></li></ul>
                </div>
    <!--头部电话-->
    <div class="tell fr">
                  
                    <p>0871-65724080</p>
                    </div>
    </div>
  </div>
  


  <v-dialog max-width="500" v-model="show_wechat_img">

  <template v-slot:default="{ isActive }" >
    <v-card>
      <v-img
      src="@/assets/connect_weixin.jpg"
    ></v-img>

      <v-card-actions style="justify-content: center;">
          <v-btn
          text="ok"
          @click="isActive.value = false"
        ></v-btn>
      </v-card-actions>
    </v-card>
  </template>
</v-dialog>

</template>

<script>
  import SvgIcon from '@jamescoyle/vue-icon';
  import { mdiPhone,mdiWechat  } from '@mdi/js';
  export default {
    components: {
      SvgIcon
    },
    methods: {
      show_wechat(){
        this.show_wechat_img = !this.show_wechat_img
      }
    },
    data() {
      return {
          show_wechat_img: false,
          phone_path: mdiPhone,
          wechat_path: mdiWechat,
      }
    }
  }
</script>

<style scoped>
.my-icon-logo {
  background: url('@/assets/logo-gray.png');
  opacity:0.5;
}
.header {
    width: 100%;
    height: 100px;
    background: #000;
}
.container {
    width: 1200px;
    margin: auto;
}
.logo.fl {
    width: 230px;
    height: 100px;
    align-items: center;
    display: flex
;
    margin-right: 54px;
}
.fl {
    float: left;
}
</style>