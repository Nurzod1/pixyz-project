<template>
  <div class="pixyz">
    <div class="container">
      <div class="pixyz-wrapper">
        <div class="pixyz-info">
          <h4 class="pixyz-title">How PixYz IT make your life easier</h4>
          <p class="pixyz-text">
            Working fast, Proactively and strategically as your trusted Managed
            Services Provider, we can take away the burden of mundane day-to-day
            tasks, protect your organization from security threats, manage your
            IT infrastructure and workloads, as well as help you to achieve an
            awful lot more - discover how PixYz IT can support you and help you
            to transform your organization Working fast, Proactively and
            strategically as your trusted Managed Services Provider, we can take
            away the burden of mundane day-to-day tasks, protect your
            organization from security threats, manage your IT infrastructure
            and workloads, as well as help you to achieve an awful lot more -
            discover how PixYz IT can support you and help you to transform your
            organization
          </p>
        </div>
        <div class="arrow-line">
          <img src="@/assets/img/arrow.png" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.pixyz {
  background-image: url(../assets/img/pixyz-back.png);
  background-repeat: no-repeat;
  background-size: 100% 105%;
  background-position-x: 0;
  background-position-y: -5px;
  position: relative;
  min-height: 100vh;

  &-wrapper {
    height: 100vh;
    display: flex;
    align-items: center;
  }

  &-info {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 31px;

    @include breakpoint(lg) {
      gap: 15px;
    }
  }

  &-title {
    font-family: "Seg-bold";
    font-size: 40px;
    color: #217a73;
    text-align: center;

    @include breakpoint(lg) {
      font-size: 35px;
    }
  }

  &-text {
    font-family: "Seg";
    font-size: 20px;
    line-height: 32px;
    color: #8a8a8a;

    @include breakpoint(lg) {
      font-size: 16px;
      line-height: 30px;
    }
  }

  .arrow-line {
    position: absolute;
    top: 50%;
    right: 50%;
    transform: translate(50%, 25%);
    z-index: 2;
    height: 360px;

    img {
      width: 100%;
      height: 100%;
    }

    @include breakpoint(lg) {
      transform: translate(50%, 55%);
      height: 180px;
    }
  }
}
</style>
