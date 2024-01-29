<template>
    <v-row class="mt-4">
        <v-col cols="12" class="text-md-left">
            <h1 class="mb-2">요금제 가격 플랜</h1>
        </v-col>
    </v-row>

    <v-sheet color="#fafafa" rounded="xl" class="py-4 px-4">
        <v-table style="background-color: transparent;">
        <thead>
        </thead>
        <tbody class="text-left">
            <tr>
                <th v-for="option in options" :key="options" v-html="option.item"></th>
            </tr>
            <tr>
                <td v-for="option in options" :key="options" v-html="option.for30"></td>
            </tr>
            <tr>
                <td v-for="option in options" :key="options" v-html="option.for90"></td>
            </tr>
        </tbody>
    </v-table>
    </v-sheet>

</template>
<script>
export default {
    name: 'PriceTable',
    data() {
        return {
            plan: ['slim', 'basic', 'plus', 'special', 'premium'],
            options: [
                {
                    item: '<b>기본 사용기간</b>',
                    for30: '30일',
                    for90: '90일',
                    for180: '180일',
                    for365: '365일',
                },
                {
                    item: '<b>추가 사용기간</b>',
                    for30: '30일',
                    for90: '60일',
                    for180: '90일',
                    for365: '90일',

                },
                {
                    item: '<b>무료 체험기간</b>',
                    for30: '14일',
                    for90: '14일',
                    for180: '14일',
                    for365: '14일',
                },
                {
                    item: '<b>총 사용기간</b>',
                    for30: '74일',
                    for90: '164일',
                    for180: '284일',
                    for365: '469일',
                },
                {
                    item: '<b>결제금액</b>',
                    for30: '50,000',
                    for90: '150,000',
                    for180: '300,000',
                    for365: '600,000',
                },


            ],
        }
    },
}
</script>