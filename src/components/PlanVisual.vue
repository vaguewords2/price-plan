<template>
  <v-sheet :stacked="false" min-height="50vh" class="visual dark  visual-top bg">
    <v-container>

          <h1 class="text-h3">중고폰 재고관리의<br/>새로운 기준, 중가비 프로</h1>
          <p>중고폰 전문가가 직접 개발한 중고폰 재고관리 시스템으로<br/>업무의 효율을 높여보세요!
          </p>
          <v-btn color="white" variant="outlined" class="my-4" rounded="xl" flat><span color="primary">소개서
              다운받기</span></v-btn>


    </v-container>
  </v-sheet>
</template>
<script>

export default {
  name: 'PlanVisual',
  data: () => ({
  })

}
</script>
<style scoped>
.bg {
  background: url('/img/2.png') no-repeat center center;
  background-size: cover;
  background-repeat: no-repeat;
}
</style>