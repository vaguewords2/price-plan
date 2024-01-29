<template>
    <v-row class="mt-4 pt-4">
        <v-col cols="12" class="text-md-left">
            <h1 class="mb-2">제공 기능</h1>
        </v-col>
    </v-row>
    <v-sheet color="#fafafa" rounded="xl" class="py-4 px-4">
        <v-table style="background-color: transparent;">
        <thead>
        </thead>
        <tbody class="text-left">
            <tr>
                <th v-for="option in options" :key="options" >{{ option.item }}</th>
                
            </tr>
            <tr>
                <td v-for="option in options" :key="options" >{{ option.pc }}</td>
            </tr>
            <tr>
                <td v-for="option in options" :key="options" >{{ option.pc }}</td>
            </tr>
            <tr>
                <td v-for="option in options" :key="options" >{{ option.pc }}</td>
            </tr>
            <tr>
                <td v-for="option in options" :key="options" >{{ option.pc }}</td>
            </tr>
        </tbody>
    </v-table>
    </v-sheet>

</template>
<script>
export default {
    name: 'PriceFunc',
    data() {
        return {
            options: [
                {
                    item: '구분',
                    pc: '',
                    for90: '90일',
                    for180: '180일',
                    for365: '365일',
                },
                {
                    item: '슬림',
                    pc: 'O',
                    for90: '14일',
                    for180: '14일',
                    for365: '14일',
                },
                {
                    item: '베이직',
                    pc: 'O',
                    for90: '164일',
                    for180: '284일',
                    for365: '469일',
                },
                {
                    item: '플러스',
                    pc: 'O',
                    for90: '150,000',
                    for180: '300,000',
                    for365: '600,000',
                },
                { 
                    item: '스페셜',
                    pc: 'O',
                    for90: '서비스 신청',
                    for180: '서비스 신청',
                    for365: '서비스 신청',
                },
                {item: '프리미엄',
                pc: 'O',}

            ],
        }
    },
}
</script>