<template>
  <div class="portfolio-items">
    <div class="portfolio-header">
      <div class="portfolio-img-wrapper">
        <p class="header-title">Portfolio</p>
      </div>
    </div>
    <div class="container">
      <div class="portfolio-wrapper">
        <portfolio-detail
          v-for="(detail, idx) in details"
          :key="idx"
          :img-url="detail.imgUrl"
          :title="detail.title"
        />
      </div>
    </div>
  </div>
</template>

<script>
import PortfolioDetail from "./PortfolioDetail.vue";
export default {
  components: { PortfolioDetail },
  data() {
    return {
      details: [
        {
          imgUrl: require("@/assets/img/portfolio-item.png"),
          title: "Business Automation",
        },
        {
          imgUrl: require("@/assets/img/portfolio-item2.jpg"),
          title: "Business Automation",
        },
        {
          imgUrl: require("@/assets/img/portfolio-item3.jpg"),
          title: "Business Automation",
        },
        {
          imgUrl: require("@/assets/img/portfolio-item4.jpg"),
          title: "Business Automation",
        },
        {
          imgUrl: require("@/assets/img/portfolio-item5.png"),
          title: "Business Automation",
        },
        {
          imgUrl: require("@/assets/img/portfolio-item6.jpg"),
          title: "Business Automation",
        },
        {
          imgUrl: require("@/assets/img/portfolio-item7.jpg"),
          title: "Business Automation",
        },
        {
          imgUrl: require("@/assets/img/portfolio-item8.jpg"),
          title: "Business Automation",
        },
        {
          imgUrl: require("@/assets/img/portfolio-item9.jpg"),
          title: "Business Automation",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.portfolio-items {
  padding-top: 71px;

  .portfolio-header {
    background-image: url(../assets/img/portfolio-img.png);
    background-repeat: no-repeat;
    background-size: cover;

    .portfolio-img-wrapper {
      display: flex;
      position: relative;
      width: 100%;
      height: 380px;
      overflow: hidden;

      &::after {
        content: "";
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        background: #217a73;
        opacity: 0.5;
      }

      .header-title {
        position: absolute;
        top: 50%;
        right: 50%;
        transform: translate(50%, -50%);
        font-family: "Seg-bold";
        font-size: 40px;
        color: #ffffff;
        z-index: 2;
      }
    }
  }

  .portfolio-wrapper {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    padding: 96px 0 100px 0;
    gap: 8px;
  }
}
</style>
