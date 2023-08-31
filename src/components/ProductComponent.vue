<template>
    <div>
        <img class="big" :src="filling.img">
        <!-- <div>
            <img @click="selectCat(user)" v-for=" user in  users" :key="user" :src="user">
        </div> -->
        <h2>{{filling.name}}</h2>
        <p>{{ filling.description }}</p>
        <p>{{ filling.price }}</p>
    </div>
</template>

<script>
export default {
    name: "ProductComponent",
    props: {
        filling: Object,
    },
}
</script>

<style lang="scss" scoped>
div {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.big {
    height: 500px;
    object-fit: cover;
}</style>