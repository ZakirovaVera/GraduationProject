<template>
    <header class="header center">
        <div class="header__left">
            <a class="header__left_logo" href="index.html">
                <img src="@/assets/img/logo_cupcake.svg" alt="ikon_logo" height="55px">
                <h2 class="header__left_logo-text">Glaze.tmn</h2>
            </a>
        </div>
        <nav class="header__right">
            <a href="#">Обо мне</a>
            <label for="burger"><svg width="32" height="23" viewBox="0 0 32 23" fill="none"
                    xmlns="http://www.w3.org/2000/svg">
                    <path d="M0 23V20.31H32V23H0ZM0 12.76V10.07H32V12.76H0ZM0 2.69V0H32V2.69H0Z" fill="#E8E8E8" />
                </svg></label>
        </nav>
        <input class="burger__checkbox" id="burger" type="checkbox">
        <div class="burger-menu">
            <div class="burger-menu_box">
                <h3 class="burger-menu__heading">MENU</h3>
                <div class="burger-menu__item">
                    <a href="catalog.html" class="burger-menu__title">Торты</a>
                    <!-- <h3 class="burger-menu__title">Торты</h3> -->
                    <ul class="burger-menu__list">
                        <li><a class="burger-menu__link" href="#">Начинки</a></li>
                        <li><a class="burger-menu__link" href="#">Оформление</a></li>
                    </ul>
                </div>
                <div class="burger-menu__item">
                    <a href="catalog.html" class="burger-menu__title">Капкейки</a>
                    <!-- <h3 class="burger-menu__title">Капкейки</h3> -->
                    <ul class="burger-menu__list">
                        <li><a class="burger-menu__link" href="#">Начинки</a></li>
                        <li><a class="burger-menu__link" href="#">Оформление</a></li>
                    </ul>
                </div>
                <div class="burger-menu__item">
                    <a href="catalog.html" class="burger-menu__title">KIDS</a>
                    <!-- <h3 class="burger-menu__title">Трайфлы</h3> -->
                    <ul class="burger-menu__list">
                        <li><a class="burger-menu__link" href="#">Начинки</a></li>
                        <li><a class="burger-menu__link" href="#">Оформление</a></li>
                    </ul>
                </div>
                <div class="burger-menu__item">
                    <a href="#" class="burger-menu__title">Эскимо / кейк-попс</a>
                </div>
                <div class="burger-menu__item">
                    <a href="#" class="burger-menu__title">Видео</a>
                </div>
                <div class="burger-menu__item">
                    <a href="#" class="burger-menu__title">Доставка</a>
                </div>
                <div class="burger-menu__item">
                    <a href="#" class="burger-menu__title">Контакты</a>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: "HeaderComponent"
}
</script>

<style lang="scss" scoped>
@import "@/assets/vars";

.center {
    padding-left: calc(50% - $siteWidth / 2);
    padding-right: calc(50% - $siteWidth / 2);
}

.box-site {
    overflow: hidden;
    position: relative;
}

.colortext {
    color: $colorSelectSite;
}

// .logo {
//     width: 35px;
//     height: 35px;
// }

.header {
    min-height: 75px;
    background: $colorFont;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    transition: background-color 0.3s;
    // position: relative;

    &__left {
        padding-left: 1rem;

        &_logo {
            display: flex;
            align-items: center;
            flex-direction: row;
            gap: 10px;
            padding-left: 4px;

            &-text {
                color: $colorSelectSite;
                font-size: 40px;
                font-weight: 400;
                line-height: 50px;
                word-wrap: break-word;
                font-family: DM Serif Display;
            }
        }
    }

    &__right {
        display: flex;
        align-items: center;
        gap: 33px;
        padding-right: 1rem;

        & a {
            color: $colorWhite;
            text-align: center;
            font-family: Jost;
            font-size: 20px;
            line-height: 25px;
            font-style: normal;
            font-weight: 400;
        }
    }

    & svg:hover path {
        fill: $colorSelectSite;
    }
}

#burger {
    position: absolute;
    left: -999999px;
    visibility: hidden;

    &:checked~.burger-menu {
        right: 0;
    }
}

.burger-menu {
    background: $colorBurgerMenu;
    width: $widthBurgerMenu;
    padding: 32px;
    box-sizing: border-box;
    box-shadow: 6px 4px 35px rgba(0, 0, 0, 0.21);
    position: absolute;
    top: 75px;
    right: -$widthBurgerMenu;
    transition: right 0.5s;
    z-index: 1;

    &__heading {
        font-style: normal;
        font-weight: 700;
        font-size: 14px;
        line-height: 17px;
        color: $colorFont;
    }

    &__item {
        display: flex;
        flex-direction: column;
        gap: 20px;
        margin-top: 20px;
    }

    &__list {
        list-style-type: none;
        padding-left: 21px;
        display: flex;
        flex-direction: column;
        gap: 11px;
    }

    &__title {
        font-style: normal;
        font-weight: 400;
        font-size: 14px;
        line-height: 17px;
        color: $colorSelectSite;
    }

    &__title:hover {
        font-weight: 700;
    }

    &__link {
        font-style: normal;
        font-weight: 400;
        font-size: 14px;
        line-height: 17px;
        color: $colorBurgerMenuText;
    }

    &__link:hover {
        color: $colorSelectSite;
    }
}
</style>