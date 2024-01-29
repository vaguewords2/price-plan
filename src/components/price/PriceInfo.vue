<script setup>
</script>
<template v-hover v-slot:default="{ isHovering, props }">
    <div class="card-price-area d-flex py-4">
        <v-card v-for="(eco, i) in pricepolicy" :key="i"
            class="card-price subheading mx-2 my-2 text-left py-4 flex-lg-fill flex-1-1-100" :class="eco.dark === 'true' ? 'dark' : ''" rounded="xl">
            
            <v-card-title>
                <v-img src="./img/logo/symbol.svg" width="32"></v-img>
                <h2>{{ eco.caption }}</h2>
                <!-- <h2 class="text-primary">{{ eco.title }}</h2> -->
            </v-card-title>
            <v-card-title>
                <h3 class="price">{{ eco.price }}<small><b>원</b> / 30일</small></h3>
            </v-card-title>
            <v-card-text>
                <h4>매입수량</h4>
                <h4>{{ eco.amount }}대 / 30일</h4>
            </v-card-text>
        </v-card>

    </div>
</template>

<script>
export default {
    name: 'PriceInfo',

    data: () => ({
        tab: null,
        cards: ['1', '2', '3', '4', '5'],
        pricepolicy: [
            {
                icon: 'mdiAccount',
                caption: 'Slim',
                title: '슬림',
                price: '30000',
                amount: '500',
                href: '',
            },
            {
                icon: '',
                caption: 'Basic',
                title: '베이직',
                price: '50000',
                amount: '1000',
                href: '',
            },
            {
                icon: '',
                caption: 'Plus',
                title: '플러스',
                price: '60000',
                amount: '5000',
                href: '',
            },
            {
                icon: '',
                caption: 'Special',
                title: '스페셜',
                price: '150000',
                amount: '10000',
                href: '',
                dark: 'true'
            },
            {
                icon: '',
                caption: 'Premium',
                title: '프리미엄',
                price: '250000',
                amount: '20000',
                href: '',
                dark: 'true'
            },
        ],

    }),
}
</script>
  