<template>
  <div class="col_2">
    <div class="img_div">
      <img :src="img_src" alt="" />
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

    img {
      width: 100%;
    }
  }
}
</style>