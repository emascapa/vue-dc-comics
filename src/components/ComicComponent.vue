<template>
  <div class="col_2">
    <div class="img_div">
      <img :src="img_src" alt="" />
      <span class="price">{{price}}</span>
    </div>
    <h6 class="text_uppercase">{{ label }}</h6>
  </div>
</template>

<script>
export default {
  name: "ComicComponent",
  props: {
    img_src: String,
    label: String,
    price: String
  },
};
</script>

<style lang="scss" scoped>
.col_2 {
  color: $light_theme;
  padding: 0.5rem;

  .img_div {
    aspect-ratio: 1;
    overflow: hidden;
    margin-bottom: 0.5rem;
    position: relative;

    &:hover {
      img {
        filter: brightness(0.2);
      }
      .price {
        display: block;
      }
    }

    img {
      width: 100%;
      cursor: pointer;
    }

    .price {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      z-index: 10;
      display: none;
    }
  }
}
</style>