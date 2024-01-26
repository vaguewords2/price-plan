<script setup>
import AboutTabItem1 from './AboutTabItem1.vue'
import AboutTabItem2 from './AboutTabItem2.vue'
import AboutTabItem3 from './AboutTabItem3.vue'
import AboutTabItem4 from './AboutTabItem4.vue'</script>
<template>
    <v-container>
        <v-row>
            <v-col cols="12">
                
    <v-tabs
      v-model="tab"
      bg-color="transparent"
      color="primary"
      grow
    >
      <v-tab value="about-1"><h3>입출고 모바일 앱</h3></v-tab>
      <v-tab value="about-2"><h3>초기비용 무료</h3>
</v-tab>
      <v-tab value="about-3"><h3>30일 단위 요금</h3></v-tab>
      <v-tab value="about-4"><h3>사용자 ID 무제한</h3></v-tab>
    </v-tabs>


      <v-window v-model="tab">
        <v-window-item value="about-1" class="text-center py-4">
            <h1>
                <AboutTabItem1/>


            </h1>
        </v-window-item>

        <v-window-item value="about-2" class="text-center py-4">

    <AboutTabItem2/>

        </v-window-item>
        <v-window-item value="about-3" class="text-center py-4">
<AboutTabItem3/>

        </v-window-item>
        <v-window-item value="about-4" class="text-center py-4">

    <AboutTabItem4/>

        </v-window-item>
      </v-window>

  
            </v-col>

        </v-row>
        <v-row>
            
        </v-row>
    </v-container>
</template>
  
<script>



export default {
    name: 'AboutTabs',

    data: () => ({
        tab: null,

    }),
}
</script>
  