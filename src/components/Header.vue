<template>
  <v-app-bar :elevation="2" scroll-behavior="hide">
    <template v-slot:image>
          <v-img
            src="@/assets/logo-gray.png"
            max-width="10%"
          ></v-img>
      </template>
    <!-- <template v-slot:prepend>
      <v-app-bar-nav-icon  icon="mdi-hammer"></v-app-bar-nav-icon>
    </template> -->

    <v-app-bar-title style="margin-left: 10%;">成都小五郎企业管理有限公司</v-app-bar-title>

    <template v-slot:append>
      <!-- <v-btn></v-btn> -->
      <!-- <v-icon :icon="`mdiSvg:${weixin}`"></v-icon> -->
      <v-btn @click="show_wechat" icon="mdi-wechat"></v-btn>
      <v-btn><svg-icon type="mdi" :path="phone_path"></svg-icon>>: 15882820920</v-btn>
    </template>
  </v-app-bar>
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
</style>