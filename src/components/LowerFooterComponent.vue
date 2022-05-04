<template>
  <section class="lower_footer">
    <div class="container">
        <div class="left_div">
            <span class="btn text_uppercase">sign-up now</span>
        </div>
        <div class="right_div d_flex align_items_center">
            <h4 class="text_uppercase">follow us</h4>
            <a v-for="(item,index) in social_icons" :key="index" href="#"><img :src="item"></a>
        </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "LowerFooterComponent",
  data: function() {
    return {
        social_icons: [
            require('@/assets/img/footer-facebook.png'),
            require('@/assets/img/footer-twitter.png'),
            require('@/assets/img/footer-youtube.png'),
            require('@/assets/img/footer-pinterest.png'),
            require('@/assets/img/footer-periscope.png'),
        ]
    }
  }
};
</script>

<style lang="scss" scoped>
.lower_footer {
    background-color: $text_dark;

    .container {
        padding: 1rem 0;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .left_div {
            .btn {
                color: $light_theme;
                border: 2px solid $primary_theme;
                font-size: 0.8rem;
            }
        }

        .right_div {
            h4 {
                color: $primary_theme;
                margin-right: 0.5rem;
                margin-bottom: 0;
                
            }
            a {
                margin-left: 0.5rem;
                img {
                    display: block;
                    max-width: 30px;
                }
            }
        }
    }
}
</style>

