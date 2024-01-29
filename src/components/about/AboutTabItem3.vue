<template>
    <v-card color="primary" class="mx-auto pt-4 px-4" rounded="xl" flat>
        <v-row justify="center" align="center">
            <v-col cols="12" xl="6" class="justify-center justify-xl-start text-center text-xl-left flex-fill">
                <v-card-title>
                    <h1>결제일 기준<br/>30일 단위 사용기간 제공</h1>
                </v-card-title>
                <v-card-subtitle>
                    중가비 프로는 결제일 기준으로 매입 수량 카운트!<br/>
1일에 결제해도 15일에 결제해도,<br/>결제일 기준 30일 동안 사용 가능!

                </v-card-subtitle>


            </v-col>
            <v-col cols="12" xl="6" class="d-flex align-end justify-center text-center flex-fill">
                <v-img max-width="45%" src="./img/app/01.png" cover class="text-white" />
            </v-col>

        </v-row>
    </v-card>
</template>
  



<script>



export default {
    name: 'AboutTabItem2',

    data: () => ({


    }),
}
</script>
  