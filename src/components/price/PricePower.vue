<script setup>
</script>
<template>
    <v-row class="py-4">
        <v-col cols="12" lg="6" v-for="pricepower in pricepowers">
            <v-card class="px-4 py-4" variant="outlined" flat>
                <v-row>
                    <v-col cols="auto" class="d-flex align-center justify-center text-center p-2">
                        <img :src="pricepower.image" width="48"/>
                    </v-col>
                    <v-col class="text-left">
                        <v-card-title class="pb-0">
                            <h3>{{ pricepower.title }}</h3>
                        </v-card-title>
                        <v-card-text>
                            {{ pricepower.caption }}
                        </v-card-text>
                    </v-col>
                </v-row>
            </v-card>
        </v-col>
    </v-row>
</template>

<script>
export default {
    name: 'PricePower',

    data: () => ({
        cards: ['1', '2', '3', '4', '5', '6'],
        pricepowers: [
            {
                image: './img/power/01.svg',
                title: '일별 재고목록',
                caption: '언제 어떤 재고를 보유했는지, 입출고된 제품은 무엇인지, 해당 재고는 언제 판매됐는지, 한눈에 확인해 보세요.'
            },
            {
                image: './img/power/02.svg',
                title: '다양한 바코드 설정',
                caption: '언제 어떤 재고를 보유했는지, 입출고된 제품은 무엇인지, 해당 재고는 언제 판매됐는지, 한눈에 확인해 보세요.'
            },
            {
                image: './img/power/03.svg',
                title: '유형별 보고서',
                caption: '언제 어떤 재고를 보유했는지, 입출고된 제품은 무엇인지, 해당 재고는 언제 판매됐는지, 한눈에 확인해 보세요.'
            },
            {
                image: './img/power/04.svg',
                title: '손쉬운 재고관리',
                caption: '언제 어떤 재고를 보유했는지, 입출고된 제품은 무엇인지, 해당 재고는 언제 판매됐는지, 한눈에 확인해 보세요.'
            },
            {
                image: './img/power/05.svg',
                title: '자동 모델 등록',
                caption: '언제 어떤 재고를 보유했는지, 입출고된 제품은 무엇인지, 해당 재고는 언제 판매됐는지, 한눈에 확인해 보세요.'
            },



            {
                image: './img/power/06.svg',
                title: '즐겨찾기 메뉴 설정',
                caption: '언제 어떤 재고를 보유했는지, 입출고된 제품은 무엇인지, 해당 재고는 언제 판매됐는지, 한눈에 확인해 보세요.'
            },
        ],

    }),
}
</script>
  