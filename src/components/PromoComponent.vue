<template>
    <section class="promo center">
        <div class="promo__img">
            <img :src="promoPhoto" alt="promo_photo">
        </div>
        <div class="promo__slogan">
            <div class="promo__info">
                <h3 class="promo__title">Добро пожаловать на сайт "{{ nameFirma }}"!</h3>
                <p class="promo__text">Я рада приветствовать вас на своем сайте. Вы можете ознакомиться с ассортиментом для заказа тортов из качественных ингредиентов с доставкой: индивидуальные торты, для семейного вечера, дня рождения, свадьбы и других событий.</p>
                <P class="promo__text">Ваш кондитер, {{ confectionersName }}.</P>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "PromoComponent",
    data() {
        return {
            nameFirma: "Glaze.tmn",
            confectionersName: "Иванова Юлия",
            promoPhoto: require('@/assets/img/promo_photo.jpg'),
        }
    },

}
</script>

<style lang="scss" scoped>
@import "@/assets/vars";

.promo {
    display: flex;
    background: $colorPromo;

    &__img {
        width: 50%;

        & img {
            width: 450px;
            height: 100%;
        }
    }

    &__slogan {
        padding-left: 64px;
        display: flex;
        align-items: center;
    }

    // &__info {
    //     border-left: 12px solid $colorSelectSite;
    //     padding-left: 16px;
    // }

    &__title {
        font-style: normal;
        font-weight: 700;
        font-size: 48px;
        line-height: 58px;
        color: $colorFont;
        padding-bottom: 28px;
    }

    &__text {
        font-style: normal;
        font-weight: 400;
        font-size: 32px;
        line-height: 38px;
        color: $colorFont;
        padding-bottom: 16px;
    }
}
</style>