<template>
  <section>
    <div class="container">
      <div class="row">
        <div class="col" v-for="(item, index) in footer_items" :key="index">
          <h3 class="text_uppercase">{{ item.label }}</h3>
          <ul>
            <li v-for="link in item.links" :key="link">{{ link }}</li>
          </ul>
        </div>
      </div>
      <img src="@/assets/img/dc-logo-bg.png" alt="" />
    </div>
  </section>
</template>

<script>
export default {
  name: "UpperFooterComponent",
  data: function () {
    return {
      footer_items: [
        {
          label: "dc comics",
          links: [
            "Characters",
            "Comics",
            "Movies",
            "TV",
            "Games",
            "Videos",
            "News",
          ],
        },
        {
          label: "shop",
          links: ["Shop DC", "Shop DC Collectibles"],
        },
        {
          label: "dc",
          links: [
            "Terms Of Use",
            "Privacy policy (New)",
            "Ad Choices",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shop Help",
            "Contact Us",
          ],
        },
        {
          label: "sites",
          links: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
//@import '@/assets/sass/variables.scss';

section {
  background-image: url(@/assets/img/footer-bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  padding: 2rem 0;
  color: white;
  height: 400px;
  overflow: hidden;

  .container {
    justify-content: space-between;
    position: relative;
    height: 100%;

    .row {
      flex-direction: column;
      height: 100%;
      align-content: flex-start;
      column-gap: 3rem;
      .col {
        //height: 100%;
        margin-bottom: 0.6rem;
        h3 {
          margin-bottom: 0.5rem;
          cursor: pointer;
        }
        ul {
          list-style: none;
          li {
            color: $secondary_font;
            font-size: 0.8rem;
            cursor: pointer;

            &:hover {
              text-decoration: underline;
            }
          }
        }
      }
    }

    img {
      position: absolute;
      top: 200px;
      right: 0;
      transform: translate(0, -50%);
      opacity: 0.5;
    }
  }
}
</style>