<template>
    <section class="product-content center">
        <!-- <h1 class="product-content__title">Начинки Тортов</h1> -->
        <div class="product-box">
            <ProductComponent v-for="filling in fillings" :key="filling.id" :fil="filling" />
        </div>
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
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta repellat ipsa dolores nesciunt magni. Veritatis libero minus ex ducimus hic.',
                    price: 1000,
                    popularity: 10,
                },
                {
                    name: "Сникерс",
                    img: require('@/assets/img/snickers.jpg'),
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta repellat ipsa dolores nesciunt magni. Veritatis libero minus ex ducimus hic.',
                    price: 1000,
                    popularity: 8,
                },
                {
                    name: "Малина",
                    img: require('@/assets/img/description-raspberries.jpg'),
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta repellat ipsa dolores nesciunt magni. Veritatis libero minus ex ducimus hic.',
                    price: 1000,
                    popularity: 7,
                },
                {
                    name: "Вишня",
                    img: require('@/assets/img/description-cherry.jpg'),
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta repellat ipsa dolores nesciunt magni. Veritatis libero minus ex ducimus hic.',
                    price: 1000,
                    popularity: 6,
                },
                {
                    name: "Клубника",
                    img: require('@/assets/img/description-strawberry.jpg'),
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta repellat ipsa dolores nesciunt magni. Veritatis libero minus ex ducimus hic.',
                    price: 1000,
                    popularity: 5,
                },
                {
                    name: "Клубника",
                    img: require('@/assets/img/description-strawberry.jpg'),
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta repellat ipsa dolores nesciunt magni. Veritatis libero minus ex ducimus hic.',
                    price: 1000,
                    popularity: 4,
                },
                {
                    name: "Клубника",
                    img: require('@/assets/img/description-strawberry.jpg'),
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta repellat ipsa dolores nesciunt magni. Veritatis libero minus ex ducimus hic.',
                    price: 1000,
                    popularity: 9,
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
@import "@/assets/vars";

.product-content {
    padding-top: 120px;
    padding-bottom: 96px;
}

.product-content__title {
    color: $colorSelectSite;
    text-align: center;
    font-family: DM Serif Display;
    font-size: 50px;
    font-style: normal;
    font-weight: 400;
    line-height: 62.5px;
    letter-spacing: 1px;
    padding-bottom: 50px;
}

.product-box {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
    justify-content: center;
}</style>