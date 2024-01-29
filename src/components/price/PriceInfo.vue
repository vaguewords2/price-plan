<script setup>
</script>
<template>
    <div class="card-price-area d-flex py-4 ga-3">
        <v-card v-for="(eco, i) in pricepolicy" :key="i"
            class="card-price subheading my-2 text-left pt-4 flex-lg-fill flex-1-1-100" :class="eco.dark === 'true' ? 'dark' : ''" rounded="xl">
            
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
            <v-card-action>
                <v-card-text><v-btn flat width="100%" rounded="xl" :class="eco.dark === 'true' ? 'bg-transparent border-white' : 'bg-primary'">플랜 보기</v-btn></v-card-text>
            </v-card-action>
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
                no: '1',
                icon: 'mdiAccount',
                caption: 'Slim',
                title: '슬림',
                price: '30,000',
                amount: '500',

            },
            { no: '2',
                icon: '',
                caption: 'Basic',
                title: '베이직',
                price: '50,000',
                amount: '1000',

            },
            { no: '3',
                icon: '',
                caption: 'Plus',
                title: '플러스',
                price: '60,000',
                amount: '5000',

            },
            { no: '4',
                icon: '',
                caption: 'Special',
                title: '스페셜',
                price: '150,000',
                amount: '10000',

                dark: 'true'
            },
            { no: '5',
                icon: '',
                caption: 'Premium',
                title: '프리미엄',
                price: '250,000',
                amount: '20000',

                dark: 'true'
            },
        ],

    }),
}
</script>
  