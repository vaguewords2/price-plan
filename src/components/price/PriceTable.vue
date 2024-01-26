<template>
    <v-table>
        <thead>
            <tr>
                <th v-for="item in desserts" :key="item" class="text-left">{{ item.name }}</th>
                
            </tr>
        </thead>
        <tbody>
            <tr v-for="item in desserts" :key="item" class="text-left">
                <td>{{ item.one }}</td>
                <td>{{ item.two }}</td>
                <td>{{ item.three }}</td>
                <td>{{ item.four }}</td>
                <td>{{ item.five }}</td>
            </tr>
        </tbody>
    </v-table>
</template>
<script>
export default {
    name: 'PriceTable',
    data() {
        return {
            desserts: [
                {
                    name: 'Slim',
                    one: 'available',
                    two: 'available',
                    three: '',
                    four: '',
                    five: ''
                },
                {
                    name: 'Basic',
                    one: 'available',
                    two: 'available',
                    three: '',
                    four: '',
                    five: ''
                },
                {
                    name: 'Plus',
                    one: 'available',
                    two: 'available',
                    three: '',
                    four: '',
                    five: ''
                },
                {
                    name: 'Special',
                    one: 'available',
                    two: 'available',
                    three: '',
                    four: '',
                    five: ''
                },
                {
                    name: 'Premium',
                    one: 'available',
                    two: 'available',
                    three: '',
                    four: '',
                    five: ''
                },

            ],
        }
    },
}
</script>