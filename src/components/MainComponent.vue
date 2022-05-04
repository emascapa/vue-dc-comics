<template>
  <main>
    <div class="jumbotron"></div>
    <div class="container">
      <span class="btn btn_primary text_uppercase upper_title">current series</span>
      <div class="row">
        <!--    <div v-for="(item, index) in comics" :key="index" class="col_2">
                <div class="img_div">
                    <img :src="item.thumb" alt="">
                </div>
                <h6 class="text_uppercase">{{item.series}}</h6>
        </div> -->
        <SiteComic v-for="(item, index) in comics" :key="index" :img_src="item.thumb" :label="item.series"/>
      </div>
      <div class="row2">
        <span class="btn btn_primary text_uppercase">load more</span>
      </div>
    </div>
  </main>
</template>

<script>
import SiteComic from '@/components/ComicComponent.vue'

export default {
  name: "MainComponent",
    components: {
    SiteComic,
  },
  data: function () {
    return {
      comics: [
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
main {
  background-color: $bg_dark;

  .jumbotron {
    height: 350px;
    background-image: url('@/assets/img/jumbotron.jpg');
    background-repeat: no-repeat;
  }

  .container {
    padding: 2.5rem 0;
    position: relative;

    .upper_title {
      position: absolute;
      top: 0;
      left: 0;
      transform: translate(0, -50%);
    }

    .row {
        //row-gap: 0.5rem;
        //column-gap: 0.5rem;
        margin-bottom: 2rem;
/*         .col_2 {
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
        } */
    }

    .row2 {
      display: flex;
      justify-content: center;
      .btn {
            font-size: 0.7rem;
      }
    }
  }
}
</style>