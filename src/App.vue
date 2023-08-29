<template>
  <HeaderComponent />
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';



export default {
  name: 'App',
  components: {
    HeaderComponent
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Lato', sans-serif;
}

img {
  max-width: 100%;
}

a {
  text-decoration: none;
}
</style>
