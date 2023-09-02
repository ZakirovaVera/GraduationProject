<template>
    <section class="products-popular center">
        <h2 class="products__heading">Популярные начинки тортов</h2>
        <div class="product-popular-box">
            <ProductComponent v-for="filling in fillingsPopular" :key="filling.id" :fil="filling" />
        </div>
    </section>
</template>

<script>
import ProductComponent from './ProductComponent.vue';
export default {
    data() {
        return {
            fillingsPopular: [
                {
                    name: "Красный бархат",
                    img: require('@/assets/img/red_velvet2.jpg'),
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta repellat ipsa dolores nesciunt magni. Veritatis libero minus ex ducimus hic.',
                    price: 1500,
                    popularity: 10,
                },
                {
                    name: "Сникерс",
                    img: require('@/assets/img/snickers.jpg'),
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta repellat ipsa dolores nesciunt magni. Veritatis libero minus ex ducimus hic.',
                    price: 1600,
                    popularity: 8,
                },
                {
                    name: "Малина",
                    img: require('@/assets/img/description-raspberries.jpg'),
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta repellat ipsa dolores nesciunt magni. Veritatis libero minus ex ducimus hic.',
                    price: 1250,
                    popularity: 7,
                },]
        }
    },
    components: {
        ProductComponent,
    }
}
</script>

<style lang="scss" scoped>
@import "@/assets/vars";
.products-popular{
    padding-top: 60px;
    padding-bottom: 96px;
}
.products__heading{
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
.product-popular-box{
    display: grid;
    grid-template-columns: repeat(auto-fill, 300px);
    gap: 40px;
    justify-content: center;
}
</style>