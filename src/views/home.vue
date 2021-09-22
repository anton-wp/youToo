<template>
  <div class="home-wrapp">
    <div class="card">
      <div class="card-title">
        <span class="card-title__text">This can be even more convenient</span>
        <img v-if="windowWidth > 576" src="@/assets/image/home.png" alt="" />
        <img v-else src="@/assets/image/homeMob.jpg" alt="" />
      </div>
      <div class="card-body">
        <span class="card-body__text"
          >Scan this code to download YouToo app on your smartphone</span
        >
        <svg width="85" height="85">
          <use xlink:href="#qr-code" />
        </svg>
        <div class="card-body__button">Switch to the app</div>
      </div>
      <div class="card-footer">
        <span>Skip for now</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      windowWidth: window.innerWidth
    };
  },
  methods: {
    onResize() {
      this.windowWidth = window.innerWidth;
    }
  },
  mounted() {
    this.$nextTick(() => {
      window.addEventListener('resize', this.onResize);
    });
  },
  beforeDestroy() {
    window.removeEventListener('resize', this.onResize);
  }
};
</script>

<style lang="scss">
@import '@/assets/scss/views/home.scss';
</style>