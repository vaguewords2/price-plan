<template>
  <div>
    <div class="d-flex justify-space-around align-center py-4">
      <v-btn variant="text" icon="mdi-minus" @click="model = Math.max(model - 1, 0)"></v-btn>
      <h1 v-for="(caption, i) in captions" :key="caption" :value="i"></h1>
      <v-btn variant="text" icon="mdi-plus" @click="model = Math.min(model + 1, 4)"></v-btn>
    </div>
    <v-carousel v-model="model">
      <v-carousel-item v-for="(color, i) in colors" :key="color" :value="i">
        <v-sheet :color="color" height="100%" tile>
          <div class="d-flex fill-height justify-center align-center">
          </div>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>




<script>
export default {
  name: 'AboutCarousel',
  data() {
    return {
      colors: [
        'primary',
        'secondary',
        'yellow darken-2',
        'red',
        'orange',
      ],
      model: 0,
      captions: ['입출고 처리 가능한 전용 모바일 앱 제공', '2', '3', '4', '5']
    }
  },
}
</script>