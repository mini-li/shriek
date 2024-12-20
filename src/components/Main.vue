<template>
  <div class="header-container" >
    <v-row justify="center" no-gutters>
      <v-col cols="1"></v-col>
      <v-col cols="2" class="header-col">
        <v-row  justify="center" no-gutters>
          <v-col cols="6">
            <v-card style="background: #000;"><v-img src="@/assets/logo-red.png" width="60%" ></v-img></v-card>
          </v-col>
          <v-col cols="6">
              <h3 style="margin-top: 13% ;">成都小五郎企业管理有限公司</h3>
          </v-col>
        </v-row> 
      </v-col>
      <v-col cols="7" justify="center">
            <!-- <v-btn variant="text" size="x-large">X-Large Button</v-btn>
            <v-btn variant="text" size="20px" style=""> 首页</v-btn> -->
        <v-tabs
          v-model="tab"
          align-tabs="center"
          color="red"
          style="margin-top:15px;margin-left:-10%;"
          
        >
          <v-tab :value="1" style="font-size:20px">首页</v-tab>
          <v-tab :value="2" style="font-size:20px">主营业务</v-tab>
          <v-tab :value="3" style="font-size:20px">案列分享</v-tab>
          <v-tab :value="4" style="font-size:20px">关于我们</v-tab>
        </v-tabs>
      </v-col>
      <v-col cols="2">
        <v-row  justify="center" no-gutters>
          <v-col cols="4">
            <v-icon
              icon="mdi-wechat"
              size="40px"
              style="margin-top: 24%"  
              @click="show_wechat_img=true"
            ></v-icon>
          </v-col>
          <v-col cols="8">
            <div style="margin-top:14%;">
              <span style="color:red; font-size:20px; ">Tel: 15882820920</span>
            </div>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>
  <div style="background:white">
    <v-divider></v-divider>
    <v-card>
    <v-tabs-window v-model="tab" hight="100%">
      <v-tabs-window-item :key="1" :value="1"> 
        <v-carousel show-arrows="hover">
          <v-carousel-item  src="@/assets/1.jpg"   cover></v-carousel-item>
          <v-carousel-item  src="@/assets/2.jpg"   cover></v-carousel-item>
          <v-carousel-item  src="@/assets/3.jpg"   cover></v-carousel-item>
          <v-carousel-item  src="@/assets/4.jpg"   cover></v-carousel-item>
          <v-carousel-item  src="@/assets/5.jpg"   cover></v-carousel-item>
          <v-carousel-item  src="@/assets/6.jpg"   cover></v-carousel-item>
          <v-carousel-item  src="@/assets/7.jpg"   cover></v-carousel-item>
          <v-carousel-item  src="@/assets/8.jpg"   cover></v-carousel-item>
        </v-carousel>
      </v-tabs-window-item>
      <v-tabs-window-item :key="2" :value="2"> <h1>主营业务</h1> </v-tabs-window-item>
      <v-tabs-window-item :key="3" :value="3"> 
        <h1>案例一</h1> 
        <span>
            2020-2023年期间，陈某担任某集团高级副总裁，集团主营业务为市政项目建设，陈某分管工程、成本，在此期间，集团作为总承包单位，在建项目合同金额60余亿元，对下劳务分包商、材料供应商签约金额40余亿元。
            2023年6月，该集团总裁委托助理联系我司，阐述了总裁听到的一些风声，但是没有实际证据，特咨询我司，希望我司给予企业管理、风险控制、监察调查技术指导。
            2023年7月，我司与该集团签订咨询协议，了解详细情况以后，我司针对性制定了监察调查、风险控制咨询方案。
            2023年8月，在我司的指导下，调查出陈某在任职高级副总裁期间，利用分管工程条线、成本条线的职务便利，与下游劳务分包商、材料供应商签订居间合同，按照产值进行提点，5-15个点不等，经调查，受贿款项少量支付至陈某个人账户，其余款项支付至陈某司机、陈某妹夫账户，另外，大量收受高档白酒、雪茄，累计受贿金额预估一千余万元，有确切证据的600余万元。
            2023年10月，该集团对陈某受贿进行报案。
        </span>
        <h1>案例二</h1>
        <span>
          2019-2024年期间，黄某任职某房地产开发公司营销副总，在此期间，该公司3个楼盘预售，累计签约金额50余亿元，通过渠道代理认购40余亿元，占比80%以上。
          2024年4月，该房地产开发公司董事会秘书联系我司，向我司阐述了近几年渠道代理费非常高，并且听到一些传言，该营销副总买豪车、在北京买房等信息，但是内部审计也进行了调查，但是没有任何的实际证据，希望我司给予审计监察技术指导。
          2024年5月，该地产公司与我司签约，签约内容为我司对其风险管理、审计监察给予咨询指导。
          2024年6月，在我司的指导下，调查出黄某在该公司任职营销副总期间，利用营销条线负责人的职务便利，私下参股渠道代理公司，承接该公司楼盘销售渠道，渠道代理费比市场价高出1-2个点，另外，私下参股家具家电公司，向该公司出售营销相关礼品，经全面调查，黄某在任职期间预计非法获利2000余万元，所有获利资金均通过外部流转。
          2024年9月，该房地产开发公司对黄某申请立案调查。
        </span>
      </v-tabs-window-item>
      <v-tabs-window-item :key="4" :value="4"> <h1>关于我们</h1> </v-tabs-window-item>
    </v-tabs-window>
  </v-card>
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
  import img_1 from "@/assets/1.jpg";
  import img_2 from "@/assets/2.jpg";
  import img_3 from "@/assets/3.jpg";
  import img_4 from "@/assets/4.jpg";
  import img_5 from "@/assets/5.jpg";
  import img_6 from "@/assets/6.jpg";
  import img_7 from "@/assets/7.jpg";
  import img_8 from "@/assets/8.jpg";

import { defineComponent, ref } from 'vue'


  export default defineComponent({
    setup() {
      const show_wechat_img = ref(false)
      const tab = ref(1)
      return {
        show_wechat_img,
        tab
      }
    } 
  })
</script>
