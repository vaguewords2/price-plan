<template>
    <v-timeline direction="horizontal">
        <v-timeline-item size="x-small" dot-color="primary" v-for="item in items" :key="item" :value="item" >
            <template v-slot:opposite>

                <small>{{item.count}}회차 결제</small>
            </template>

                <small><b>{{item.date}}</b></small>
                    


            <div>
                

            </div>
        </v-timeline-item>


    </v-timeline>
</template>
<script>
export default {
    name: 'AboutTimelineWrong',
    data: () => ({
        items: [
        {date: '1/30', count: '1'},
        {date: '2/1', count: '2'},
        {date: '3/1', count: '3'}
    ]
    })

}
</script>