<template>
  <div class="pixzy-techno">
    <div class="container">
      <div class="pixzy-techno-wrapper">
        <div class="techno-title">
          <h5>Specialties and Technologies</h5>
          <p>
            Our stratigists, designers, architectecs, developers and quality
            analysts excel in every technology powering native, hybrid, cross-
            platform and custom software development.
          </p>
          <div class="round-img-wrapper">
            <img src="@/assets/img/round.png" alt="" />
          </div>
        </div>
        <div class="technologies">
          <techno-type
            v-for="(techno, idx) in technos"
            :key="idx"
            :img-url="techno.imgUrl"
            :title="techno.title"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TechnoType from "./TechnoType.vue";
export default {
  components: {
    TechnoType,
  },
  data() {
    return {
      technos: [
        { imgUrl: require("@/assets/img/js.svg"), title: "JS" },
        { imgUrl: require("@/assets/img/python.svg"), title: "Python" },
        { imgUrl: require("@/assets/img/ror.svg"), title: "ROR" },
        { imgUrl: require("@/assets/img/spec_13.svg"), title: "Ruby" },
        { imgUrl: require("@/assets/img/mysql.svg"), title: "MySQl" },
        { imgUrl: require("@/assets/img/java.svg"), title: "Java" },
        { imgUrl: require("@/assets/img/in.svg"), title: "IN" },
        { imgUrl: require("@/assets/img/aws.svg"), title: "AWS" },
        { imgUrl: require("@/assets/img/laravel.svg"), title: "Laravel" },
        { imgUrl: require("@/assets/img/basecamp.svg"), title: "BaseCamp" },
        { imgUrl: require("@/assets/img/xaskell.svg"), title: "Xaskell" },
        { imgUrl: require("@/assets/img/react.svg"), title: "React" },
        { imgUrl: require("@/assets/img/android.svg"), title: "Android" },
        { imgUrl: require("@/assets/img/css.svg"), title: "CSS 3" },
        { imgUrl: require("@/assets/img/js.svg"), title: "JS" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.pixzy-techno {
  padding: 100px 0;

  @include breakpoint(lg) {
    padding: 80px 0;
  }

  .techno-title {
    position: relative;
    display: flex;
    flex-direction: column;
    gap: 28px;
    margin-bottom: 56px;

    @include breakpoint(lg) {
      gap: 15px;
      margin-bottom: 40px;
    }

    h5 {
      font-family: "Seg-bold";
      font-size: 40px;
      color: #217a73;
      text-align: center;

      @include breakpoint(lg) {
        font-size: 35px;
      }
    }

    p {
      font-family: "Seg";
      font-size: 24px;
      color: #8a8a8a;

      @include breakpoint(lg) {
        font-size: 20px;
      }
    }

    .round-img-wrapper {
      position: absolute;
      top: 10%;
      left: 0;
      transform: translate(-15%);
      z-index: -1;
    }
  }

  .technologies {
    display: grid;
    grid-template-columns: repeat(8, 1fr);
    gap: 35.5px;

    @include breakpoint(lg) {
      grid-template-columns: repeat(5, 1fr);
    }
  }

  .techno-type {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 104px;
    height: 120px;
    gap: 10px;
    border: 1px solid #ffffff;
    border-radius: 10px;
    padding: 25px;
    background: #ffffff;

    &:hover {
      border: 1px solid #49d6cb;
      filter: drop-shadow(3px 3px 30px rgba(0, 0, 0, 0.161));

      .name {
        opacity: 1;
      }
    }

    .name {
      font-family: "Seg";
      font-size: 16px;
      color: #7d7d7d;
      opacity: 0;
      white-space: nowrap;
    }
  }
}
</style>
