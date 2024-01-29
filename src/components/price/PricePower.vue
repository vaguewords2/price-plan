<script setup>
</script>
<template>
    <v-row class="py-4">
        <v-col cols="12" xl="4" lg="6" v-for="pricepower in pricepowers">
            <v-card class="px-4 py-4 d-flex align-center" flat style="background-color: #fafafa; height: 100%" rounded="xl">
                <v-row no-gutters>
                    <v-col cols="auto" class="d-flex align-center justify-center text-center p-2">
                        <img :src="pricepower.image" width="48"/>
                    </v-col>
                    <v-col class="text-left">
                        <v-card-title class="pb-0">
                            <h3>{{ pricepower.title }}</h3>
                        </v-card-title>
                        <v-card-text v-html="pricepower.caption">
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
                caption: '언제 어떤 재고를 보유했는지, 입출고된 제품은 무엇인지,<br/>해당 재고는 언제 판매됐는지 한눈에 확인해 보세요.'
            },
            {
                image: './img/power/02.svg',
                title: '다양한 바코드 설정',
                caption: '재고관리부터 출고까지<br/>필요 용도에 따라 바코드를 설정하여 관리해 보세요.<Br/><small>(재고관리용, 라벨용, 출고용)</small>'
            },
            {
                image: './img/power/03.svg',
                title: '유형별 보고서',
                caption: '매입/출고/판매부터 정산, 제품까지<br/>상세한 보고서가 자동 생성됩니다.<br/><small>(일자, 모델, 업체, 전표, 등급, 보관위치 등 통계 제공)</small>'
            },
            {
                image: './img/power/04.svg',
                title: '손쉬운 재고관리',
                caption: '재고이동, 재고 시세 비교 등으로<br/>효율적인 재고관리가 가능합니다.'
            },
            {
                image: './img/power/05.svg',
                title: '자동 모델 등록',
                caption: 'USB만 연결하면 자동으로 모델정보가 등록되어<br/>빠른 제품 등록이 가능합니다.<br/><small>(모델명, 모델번호, 용량, 색상(애플만 지원))</small>'
            },
            {
                image: './img/power/06.svg',
                title: '즐겨찾기 메뉴 설정',
                caption: '사용자가 자주 사용하는 메뉴를 설정하면<br/>화면 상단에 메뉴가 노출되고 단축키가 자동 설정됩니다.'
            },
        ],

    }),
}
</script>
  