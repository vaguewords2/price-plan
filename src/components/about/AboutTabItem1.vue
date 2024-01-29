<template>
    <v-card color="primary" class="mx-auto pt-4 px-4" rounded="xl" flat>
        <v-row justify="center" align="center">
            <v-col cols="12" xl="6" class="justify-center justify-xl-start text-center text-xl-left flex-fill">
                <v-card-title>
                    <h1>입출고 처리 가능한<br />전용 모바일 앱 제공</h1>
                </v-card-title>
                <v-card-subtitle>
                    PC/태플릿/스마트폰 모든 기종 지원
                </v-card-subtitle>
                <v-card-text>
                    <v-card-action class="d-block mb-2">
                        <v-btn color="white" size="large" rounded="xl" align="center" flat>
                            <v-img src="./img/logo/symbol.svg" width="32px"></v-img>
                            &nbsp; Joongabi PRO PC
                        </v-btn>
                    </v-card-action>
                    <v-card-action class="me-2">
                        <v-btn color="white" size="large" rounded="xl" align="center" flat>
                            <v-img src="./img/logo/symbol.svg" width="32px"></v-img>
                            &nbsp; Google Play
                        </v-btn>
                    </v-card-action>
                    <v-card-action>
                        <v-btn color="white" size="large" rounded="xl" align="center" flat>
                            <v-img src="./img/logo/symbol.svg" width="32px"></v-img>
                            &nbsp; AppStore
                        </v-btn>
                    </v-card-action>
                </v-card-text>


            </v-col>
            <v-col cols="12" xl="6" class="d-flex align-end justify-center text-center flex-fill">
                <v-img max-width="45%" src="./img/app/01.png" cover class="text-white" />
            </v-col>

        </v-row>
    </v-card>
</template>
  



<script>



export default {
    name: 'AboutTabItem1',

    data: () => ({


    }),
}
</script>
  