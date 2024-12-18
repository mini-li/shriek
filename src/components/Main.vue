<template>
  
  <v-card>
    <v-tabs
      v-model="tab"
      align-tabs="center"
      color="deep-purple-accent-4"
    >
      <v-tab :value="1">首页</v-tab>
      <v-tab :value="2">主营业务</v-tab>
      <v-tab :value="3">案列分享</v-tab>
      <v-tab :value="4">关于我们</v-tab>
    </v-tabs>

    <v-tabs-window v-model="tab">
      <v-tabs-window-item :key="1" :value="1"> 
        <v-carousel>
          <v-carousel-item 
            v-for="i in tab"
            :key="i.key"
            :src="i.url"
            cover
          ></v-carousel-item>
        </v-carousel>
      </v-tabs-window-item>
      <v-tabs-window-item :key="2" :value="2"> <h1>主营业务</h1> </v-tabs-window-item>
      <v-tabs-window-item :key="3" :value="3"> <h1>案列分享</h1> </v-tabs-window-item>
      <v-tabs-window-item :key="4" :value="4"> <h1>关于我们</h1> </v-tabs-window-item>
      <!-- <v-tabs-window-item
        v-for="n in 4"
        :key="n"
        :value="n"
      >
        <v-container fluid>
          <v-row>
            <v-col
              v-for="i in 6"
              :key="i"
              cols="12"
              md="4"
            >
              <v-img
                :lazy-src="`https://picsum.photos/10/6?image=${i * n * 5 + 10}`"
                :src="`https://picsum.photos/500/300?image=${i * n * 5 + 10}`"
                height="205"
                cover
              ></v-img>
            </v-col>
          </v-row>
        </v-container>
      </v-tabs-window-item> -->
    </v-tabs-window>
  </v-card>
  v-container
  <v-img
    :width="300"
    aspect-ratio="16/9"
    cover
    :src="img_1"
  ></v-img>
 
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

  export default {
    data: () => ({
      tab: [
      {img:img_1,key:"1"},
      {img:img_2,key:"2"},
      {img:img_3,key:"3"},
      {img:img_4,key:"4"},
      {img:img_5,key:"5"},
      {img:img_6,key:"6"},
      {img:img_7,key:"7"},
      {img:img_8,key:"8"},
 

    ]
    }),
  }
</script>
