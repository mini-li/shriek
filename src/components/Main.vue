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
            v-for="i in 8"
            :key="i"
            :src="`src/assets/${i}.jpg`"
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

 
</template>

<script>
  export default {
    data: () => ({
      tab: null,
    }),
  }
</script>
