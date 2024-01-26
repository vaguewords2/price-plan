<script setup>
import PlanVisual from './PlanVisual.vue';
import AboutVisual from './about/AboutVisual.vue';
import AboutTabs from './about/AboutTabs.vue';
import PriceInfo from './price/PriceInfo.vue';
import PriceVisual from './price/PriceVisual.vue';
import PriceTable from './price/PriceTable.vue';
</script>
<template>
    <PlanVisual />
    <v-container>
        <v-row>
            <v-col cols="12">
                <v-tabs v-model="tab" bg-color="transparent" color="primary" grow>
                    <v-tab value="one">중가비 프로 소개</v-tab>
                    <v-tab value="two">가격정책</v-tab>
                </v-tabs>
            </v-col>
        </v-row>
        <v-window v-model="tab">
            <v-window-item value="one" class="text-center">
                <AboutVisual />
                <AboutTabs />
            </v-window-item>

            <v-window-item value="two" class="text-center">

                <PriceVisual />
                <PriceInfo />
                <PriceTable />

            </v-window-item>

        </v-window>




    </v-container>
</template>
  
<script>



export default {
    name: 'Plan',

    data: () => ({
        tab: null,

    }),
}
</script>
  