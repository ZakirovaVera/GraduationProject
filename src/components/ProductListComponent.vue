<template>
    <section class="product center">
        <ProductComponent v-for="filling in fillings" :key="filling.id" :filling="filling" />
    </section>
</template>

<script>
import ProductComponent from './ProductComponent.vue';
export default {
    name: 'ProductListComponent',
    data() {
        return {
            fillings: [
                {
                    name: "Красный бархат",
                    img: require('@/assets/img/red_velvet2.jpg'),
                    description: 'lorem',
                    price: 1000,
                },
                {
                    name: "Сникерс",
                    img: require('@/assets/img/snickers.jpg'),
                    description: 'lorem',
                    price: 1000,
                },
                {
                    name: "Малина",
                    img: require('@/assets/img/description-raspberries.jpg'),
                    description: 'lorem',
                    price: 1000,
                },
                {
                    name: "Вишня",
                    img: require('@/assets/img/description-cherry.jpg'),
                    description: 'lorem',
                    price: 1000,
                },
                {
                    name: "Клубника",
                    img: require('@/assets/img/description-strawberry.jpg'),
                    description: 'lorem',
                    price: 1000,
                },
            ]
        }
    },

    components: {
        ProductComponent,
    }
}
</script>

<style lang="scss" scoped>
.product
{
    display: grid;
    grid-template-columns: repeat(auto-fill, 300px);
    gap: 10px;
    justify-content: center;
}</style>