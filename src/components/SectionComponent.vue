<template>
    <section>
        <div class="container">
            <div class="row">
                <div class="col d_flex align_items_center text_uppercase" v-for="({img_src, caption}, index) in section_items" :key="index">
                    <img :src="img_src">
                    <span>{{caption}}</span>
                </div>
            </div>

        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionComponent',
    data: function() {
        return {
            section_items: [
                {
                    img_src: require('@/assets/img/buy-comics-digital-comics.png'),
                    caption: 'digital comics'
                },
                {
                    img_src: require('@/assets/img/buy-comics-merchandise.png'),
                    caption: 'dc merchandise'
                },
                {
                    img_src: require('@/assets/img/buy-comics-subscriptions.png'),
                    caption: 'subscription'
                },
                {
                    img_src: require('@/assets/img/buy-comics-shop-locator.png'),
                    caption: 'comic shop locator'
                },
                {
                    img_src: require('@/assets/img/buy-dc-power-visa.svg'),
                    caption: 'dc power visa'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
//@import '@/assets/sass/variables.scss';


    section {
        background-color: $primary_theme;

        color: $light_theme;
        font-size: 0.7rem;

        padding: 2rem 1rem;

        .container {

            img {
                max-width: 40px;
                max-height: 40px;
            }

            .col {
                span {
                    margin-left: 0.5rem;
                    cursor: pointer;
                }
            }
        }
    }
</style>

