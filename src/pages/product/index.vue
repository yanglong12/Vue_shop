<template>
  <div class="product">
    <me-product-nav>
      <i @click="goBack" slot="left" class="iconfont icon-back product-back"></i>
      <div class="product-title" slot="center">商品详情</div>
      <i slot="right" class="iconfont icon-cart product-back"></i>
    </me-product-nav>
  </div>
</template>

<script>
  import MeProductNav from 'base/navbar';
  // import MeSlider from 'base/slider';
  export default {
    name: 'Product',
    components: {
      MeProductNav
    },
    data() {
      return {};
    },
    created() {
      this.init();
    },
    methods: {
      goBack() {
        this.$router.back();
      },
      init() {}
    }
  };
</script>

<style lang="scss" scoped>
@import "~assets/scss/mixins";
.product {
  overflow: hidden;
  position: absolute;
  top: 0;
  left: 0;
  z-index: $product-z-index;
  width: 100%;
  height: 100%;
  background-color: $bgc-theme;
  .mine-navbar {
    background-color: $header-bgc;

    .product-back,
    .product-title {
      color: #fff;
    }
    .product-title {
      text-align: center;
    }
  }
}
</style>
