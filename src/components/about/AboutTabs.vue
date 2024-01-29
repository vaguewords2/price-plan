<script setup>
import PriceInfo from '../price/PriceInfo.vue'
import PricePower from '../price/PricePower.vue'
import AboutTimelineWrong from './AboutTimelineWrong.vue'
import AboutTimelineCorrect from './AboutTimelineCorrect.vue'
</script>
<template>
    <v-container>
        <v-row>
            <v-col cols="12">


                <v-tabs v-model="tab" bg-color="transparent" color="primary" grow>
                    <v-tab v-for="item in items" :key="item" :value="item">
                        {{ item.title }}
                    </v-tab>
                </v-tabs>

                <v-window v-model="tab">
                    <v-window-item v-for="item in items" :key="item" :value="item" class="py-4">
                        <v-card color="primary" class="mx-auto px-5 my-4" rounded="xl" flat>
                            <v-row justify="center" align="center" class="px-5">

                                <v-col cols="12" xl="6"
                                    class="justify-center justify-xl-start text-center text-xl-left flex-fill my-4 py-4">
                                    <h1 class="banner-title mb-2" v-html="item.content"></h1>
                                    <v-card-subtitle v-html="item.caption" class="px-0"></v-card-subtitle>
                                </v-col>
                                <v-col cols="12" xl="6" class="d-flex align-end justify-center text-center flex-fill mt-4">
                                    <v-img src="./img/app/01.png" v-if="item.no ==='1'" max-width="40%"></v-img>
                                    <v-img src="./img/app/02.png" v-if="item.no ==='2'" max-width="40%"></v-img>
                                    <v-row v-if="item.no === '3'" class="mb-4">
                                        <v-col cols="12" style="opacity: 0.35">
                                            <AboutTimelineWrong/>
                                        </v-col>
                                        <v-col cols="12">
                                            <AboutTimelineCorrect/>
                                        </v-col>
                                    </v-row>
                                    <v-img src="./img/app/01.png" v-if="item.no ==='4'" max-width="40%"></v-img>
                                </v-col>
                            </v-row>


                        </v-card>
                    </v-window-item>
                </v-window>

            </v-col>

            <v-col cols="12" class="text-md-left">
                <h1>중가비 프로 서비스 요금 플랜</h1>
                <PriceInfo></PriceInfo>
            </v-col>
            <v-col cols="12" class="text-md-left">
                <h1>중가비 프로 핵심 경쟁력</h1>
                <v-rows>
                    <PricePower />
                </v-rows>
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
        tab: 'About',
        items: [
            { no: '1', title: '입출고 모바일 앱', content: '입출고 처리 가능한<br/>전용 모바일 앱 제공', caption: 'PC/태플릿/스마트폰 모든 기종 지원' },
            { no: '2', title: '초기비용 무료', content: '중가비 프로<br/>모든 요금제 초기비용 무료!', caption: '초기비용 부담 없이 요금제만 결제하면 사용 가능' },
            { no: '3', title: '30일 단위 요금', content: '결제일 기준<br/>30일 단위 사용기간 제공', caption: '중가비 프로는 결제일 기준으로 매입 수량 카운트!<br/>1일에 결제해도 15일에 결제해도,<br/>결제일 기준 30일 동안 사용 가능!',
            image: '<v-timeline direction="horizontal"><AboutTimeline/></v-timeline>' },
            { no: '4', title: '사용자 ID 무제한', content: '개수 제한 없이<br/>사용자 무제한 생성', caption: '회사 마스터계정 1개만 가입하면<br/>사용자 계정은 무제한 생성하고<br/>업무에 맞춰 메뉴별 권한 설정 기능 제공' },
        ],

    }),
}
</script>
  