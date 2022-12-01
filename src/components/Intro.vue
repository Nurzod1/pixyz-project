<template>
  <div class="intro">
    <div class="container">
      <div class="intro-wrapper">
        <div class="intro-title-wrapper">
          <div class="title-img-wrapper">
            <img src="@/assets/img/title-img.png" alt="" />
          </div>
          <h1 class="intro-title">
            Digital Agency <br />
            and Marketing
          </h1>
          <div class="title-round-wrapper">
            <img src="@/assets/img/title-round.png" alt="" />
          </div>
          <p class="intro-text">
            Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam
            nonumy eirmod
          </p>
        </div>
        <div class="intro-image-wrapper">
          <img src="@/assets/img/intro-img.png" alt="" />
        </div>
        <div class="icon-phone">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="28.311"
            height="28.311"
            viewBox="0 0 28.311 28.311"
          >
            <path
              id="ic_perm_phone_msg_24px"
              d="M4.573,22.66a17.868,17.868,0,0,0,5.615-.9,1.605,1.605,0,0,1,1.6.377l3.46,3.46A23.709,23.709,0,0,0,25.617,15.252l-3.46-3.476a1.544,1.544,0,0,1-.393-1.589,17.867,17.867,0,0,0,.9-5.615A1.577,1.577,0,0,1,24.233,3h5.5a1.577,1.577,0,0,1,1.573,1.573A26.735,26.735,0,0,1,4.573,31.31,1.577,1.577,0,0,1,3,29.738v-5.5A1.577,1.577,0,0,1,4.573,22.66ZM17.155,3V18.728L12.437,14.01H3V3Z"
              transform="translate(-3 -3)"
              fill="#fff"
            />
          </svg>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.intro {
  display: flex;
  background-image: url(../assets/img/intro-back.png);
  background-repeat: no-repeat;
  background-size: 100% 100%;
  background-position-x: 0;
  background-position-y: 5px;
  padding-top: 100px;
  min-height: 100vh;

  @include breakpoint(xs) {
    background-image: none;
  }

  &-wrapper {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
  }

  &-title-wrapper {
    width: 50%;
    position: relative;
    margin-left: 35px;

    @include breakpoint(sm) {
      margin-left: 0;
    }

    .intro-title {
      font-family: "Seg-bold";
      font-size: 56px;
      color: #000000;
      margin-bottom: 25px;

      @include breakpoint(lg) {
        font-size: 45px;
        margin-bottom: 20px;
      }
      @include breakpoint(md) {
        font-size: 35px;
        margin-bottom: 13px;
      }

      @include breakpoint(sm) {
        font-size: 30px;
      }

      @include breakpoint(xs) {
        font-size: 20px;
        margin-bottom: 10px;
      }
    }

    .intro-text {
      font-family: "Seg";
      font-size: 24px;
      color: #000000;

      @include breakpoint(lg) {
        font-size: 22px;
      }

      @include breakpoint(md) {
        font-size: 18px;
      }

      @include breakpoint(xs) {
        font-size: 13px;
      }
    }

    .title-img-wrapper {
      position: absolute;
      top: 30%;
      left: -10%;

      @include breakpoint(lg) {
        top: 20%;
      }

      @include breakpoint(md) {
        display: none;
      }
    }

    .title-round-wrapper {
      position: absolute;
      left: 25%;
      bottom: 25%;
      z-index: -1;

      @include breakpoint(lg) {
        bottom: 5%;
      }

      @include breakpoint(md) {
        bottom: -10%;
      }
      @include breakpoint(md) {
        bottom: -10%;
        left: 0;
      }

      @include breakpoint(sm) {
        display: none;
      }
    }
  }

  &-image-wrapper {
    width: 50%;
    width: 600px;
    height: 400px;
    img {
      width: 100%;
      height: 100%;
    }

    @include breakpoint(lg) {
      width: 500px;
      height: 300px;
    }

    @include breakpoint(md) {
      width: 430px;
      height: 240px;
    }

    @include breakpoint(sm) {
      width: 250px;
      height: 150px;
    }
  }

  .icon-phone {
    position: fixed;
    bottom: 7%;
    right: 10%;
    width: 58px;
    height: 58px;
    padding: 17px 15px 15px 20px;
    border-radius: 50%;
    color: rgba(12, 180, 166, 0.35);
    background: #49d6cb;
    box-shadow: 0 0 0 rgba(204, 169, 44, 0.4);
    cursor: pointer;
    animation: pulse 1s infinite;
    z-index: 9999;

    svg {
      width: 100%;
      height: 100%;
    }
    @keyframes pulse {
      0% {
        -webkit-box-shadow: 0 0 0 0 rgba(92, 236, 168, 0.4);
      }
      70% {
        -webkit-box-shadow: 0 0 0 10px rgba(79, 226, 185, 0);
      }
      100% {
        -webkit-box-shadow: 0 0 0 0 rgba(89, 230, 199, 0);
      }
    }

    @keyframes pulse {
      0% {
        -moz-box-shadow: 0 0 0 0 rgba(120, 228, 194, 0.4);
        box-shadow: 0 0 0 0 rgba(36, 211, 191, 0.4);
      }
      70% {
        -moz-box-shadow: 0 0 0 10px rgba(204, 169, 44, 0);
        box-shadow: 0 0 0 10px rgba(204, 169, 44, 0);
      }
      100% {
        -moz-box-shadow: 0 0 0 0 rgba(204, 169, 44, 0);
        box-shadow: 0 0 0 0 rgba(204, 169, 44, 0);
      }
    }
  }
}
</style>
