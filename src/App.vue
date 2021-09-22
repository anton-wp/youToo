<template>
  <div id="app">
    <SvgCustom />
    <DefLayout />
    <Home />
  </div>
</template>

<script>
import DefLayout from "@/layout/default.vue"
import Home from "@/views/home.vue"
import SvgCustom from "@/components/svg.vue"

export default {
  name: 'App',
  components: {
    DefLayout,
    Home,
    SvgCustom
  }
}
</script>

<style lang="scss">
@import "@/assets/scss/global.scss";

</style>
