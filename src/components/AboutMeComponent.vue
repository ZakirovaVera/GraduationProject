<template>
    <img :src="imgAboutMe" alt="photo">
</template>

<script>
    export default {
        data() {
            return {
                imgAboutMe: require('@/assets/img/aboutMe.jpg'),
            }
        },
    }
</script>

<style lang="scss" scoped>
@import "@/assets/vars";

</style>