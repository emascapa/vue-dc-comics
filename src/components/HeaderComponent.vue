<template>
    <header>
      <div class="container d_flex align_items_center">
          <div class="logo">
          <img src="@/assets/img/dc-logo.png" alt="">
          </div>
          
        <ul class="d_flex align_items_center">
            <li v-for="(item, index) in header_items" :key="index" class="d_flex align_items_center" :class="active_counter == index ? 'active' : ''">{{item}}</li>
        </ul>
          
      </div>
    </header>
</template>

<script>
export default {
    name: 'HeaderComponent',
    data: function() {
        return {
            active_counter: 1,
            header_items: [
                'characters','comics','movie','tv','games','collectibles','videos','fans','news','shop'
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
//@import '@/assets/sass/variables.scss';

    header {
        background-color: $light_theme;
        padding: 0 1rem;
        height: 80px;


        .container {
            justify-content: space-between;
            height: 100%;

            .logo {
                padding: 1rem 0;
                height: 100%;

                img {
                max-height: 100%;
                }
            }
    
            ul {
                list-style: none;
                height: 100%;
                li {
                    height: 100%;
                    margin-left: 1.5rem;
                    font-size: 0.8rem;
                    text-transform: uppercase;
                    font-family: $custom_font;
                    border-bottom: 4px solid $light_theme;

                    cursor: pointer;

                    &.active{
                        color: $primary_theme;
                        border-color: $primary_theme;
                    }

                    &:hover {
                        color: $primary_theme;
                        border-color: $primary_theme;
                    }
                }
            }
        }
    }
</style>