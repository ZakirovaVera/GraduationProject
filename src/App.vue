<template>
  <div class="box-site">
    <HeaderComponent :storageData="storages" />
    <BannerComponent v-if="isPageAboutMe || isProductList" :storageData="storages" />

    <!-- Главная -->
    <PromoComponent v-if="isPageIndex" />
    <PopularGoodsComponent v-if="isPageIndex" />
    <!-- Начинки -->
    <ProductListComponent v-if="isProductList" />
    <!-- Обо мне -->
    <AboutMeComponent v-if="isPageAboutMe" />

    <FooterComponent :storageData="storages"/>
  </div>
</template>

<script>
import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import PromoComponent from './components/PromoComponent.vue';
import ProductListComponent from './components/ProductListComponent.vue';
import PopularGoodsComponent from './components/PopularGoodsComponent.vue';
import BannerComponent from './components/BannerComponent.vue';
import AboutMeComponent from './components/AboutMeComponent.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    PromoComponent,
    FooterComponent,
    ProductListComponent,
    PopularGoodsComponent,
    BannerComponent,
    AboutMeComponent
  },
  data() {
    return {
      storages: {
        currentPage: "",
      }
    }
  },
  computed: {
    isPageIndex: function () {
      return this.storages.currentPage === 'index';
    },
    isPageAboutMe: function () {
      return this.storages.currentPage === 'aboutme';
    },
    isProductList: function () {
      return this.storages.currentPage === 'productList';
    },
  }
}
</script>

<style lang="scss">
@import "@/assets/vars";

* {
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Lato', sans-serif;
}

.center {
  padding-left: calc(50% - $siteWidth / 2);
  padding-right: calc(50% - $siteWidth / 2);
}

// img {
//   max-width: 100%;
// }

a {
  text-decoration: none;
}

.box-site {
  overflow: hidden;
  position: relative;
}
</style>
