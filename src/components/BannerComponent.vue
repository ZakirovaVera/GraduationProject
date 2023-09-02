<template>
    <div class="banner center">
        <div class="banner__title">
            <h1 class="banner__heading">{{ getBannerText }}</h1>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        storageData: Object
    },
    computed: {
        getBannerText: function () {
            let currentPageTag = this.storageData.currentPage;
            if (currentPageTag === "index") {
                return "Главная";
            }
            if (currentPageTag === "aboutme") {
                return "Обо мне";
            }
            if (currentPageTag === "video") {
                return "Видеоблог";
            }
            if (currentPageTag === "contacts") {
                return "Контакты";
            }
            if (currentPageTag === "productList") {
                return "Начинки";
            }

            return "Не определено";
        },
    },
}
</script>

<style lang="scss" scoped>
@import "@/assets/_vars.scss";

.banner {
    // background: url(<path-to-image>), lightgray 50% / cover no-repeat;
    background-image: url(@/assets/img/banner2.jpg);
    background-size: cover;
    background-position: center;
    height: 356px;
    display: flex;
    align-items: flex-end;
    justify-content: center;

    &__title {
        border-radius: 37px 37px 0px 0px;
        background: #FFF;
        display: flex;
        width: 503px;
        padding: 41px 78px;
        flex-direction: column;
        align-items: center;
        gap: 10px;
    }

    &__heading {
        color: $colorBackground;
        font-size: 50px;
        font-family: DM Serif Display;
        font-weight: 400;
        line-height: 62.50px;
    }

    &__text {
        color: $colorFont;
        font-size: 22px;
        font-family: Jost;
        font-weight: 400;
        line-height: 33px;
        letter-spacing: 0.22px;
    }
}
</style>