<template>
    <v-timeline direction="horizontal">
        <v-timeline-item size="x-small" dot-color="primary" v-for="item in items" :key="item" :value="item" >
            <template v-slot:opposite>
                
                    <p v-html="item.count"></p>
                
                
            </template>
            
            <h2><b>{{item.date}}</b></h2>
            <div>
                

            </div>
        </v-timeline-item>


    </v-timeline>
</template>
<script>
export default {
    name: 'AboutTimelineCorrect',
    data: () => ({
        items: [
        {date: '1/30', count: '1회차 결제'},
        {date: '2/1', count: '중가비 프로는<br><b>30일 단위 결제!</b>'},
        {date: '3/1', count: '2회차 결제'}
    ]
    })

}
</script>