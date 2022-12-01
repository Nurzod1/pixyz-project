<template>
  <div class="service-info">
    <div class="service-header">
      <div class="service-img-wrapper">
        <!-- <img src="@/assets/img/service-img.png" alt="" /> -->
        <p class="header-title">Services</p>
      </div>
    </div>
    <div class="container">
      <div class="service-info-wrapper">
        <development
          v-for="(service, idx) in services"
          :key="idx"
          :title="service.title"
        >
          <div class="development-type-wrapper">
            <development-type
              v-for="(card, idx) in service.cards"
              :key="idx"
              :title="card.title"
              :content="card.content"
              :price="card.price"
            />
          </div>
        </development>
      </div>
    </div>
  </div>
</template>

<script>
import Development from "@/components/Development.vue";
import DevelopmentType from "@/components/DevelopmentType.vue";
export default {
  components: { Development, DevelopmentType },
  data() {
    return {
      services: [
        {
          title: "Web Development",
          cards: [
            {
              title: "Landing Page",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Site Catalog",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Corporative Site",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Landing Page",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Site Catalog",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Corporative Site",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
          ],
        },
        {
          title: "Mobile Development",
          cards: [
            {
              title: "Landing Page",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Site Catalog",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Corporative Site",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Landing Page",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Site Catalog",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Corporative Site",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
          ],
        },
        {
          title: "Business Automation",
          cards: [
            {
              title: "Landing Page",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Site Catalog",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Corporative Site",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Landing Page",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Site Catalog",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Corporative Site",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
          ],
        },
        {
          title: "UX/UI Design",
          cards: [
            {
              title: "Landing Page",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Site Catalog",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Corporative Site",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Landing Page",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Site Catalog",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Corporative Site",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
          ],
        },
        {
          title: "Digital Marketing",
          cards: [
            {
              title: "Landing Page",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Site Catalog",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Corporative Site",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Landing Page",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Site Catalog",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
            {
              title: "Corporative Site",
              content:
                "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd",
              price: 6000000,
            },
          ],
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.service-info {
  padding-top: 71px;

  &-wrapper {
    padding: 100px 0;
  }

  .service-header {
    background-image: url(../assets/img/service-img.png);
    background-repeat: no-repeat;
    background-size: cover;

    .service-img-wrapper {
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

  .development-type-wrapper {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    column-gap: 47px;
    row-gap: 32px;
  }
}
</style>
