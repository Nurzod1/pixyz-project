<template>
  <div class="get-touch">
    <div class="container">
      <div class="get-touch-wrapper">
        <div class="main-wrapper">
          <form class="get-touch-body">
            <h5 class="get-touch-title">Get in Touch</h5>
            <div class="input-wrapper">
              <input type="text" placeholder="Name" />
              <input type="text" placeholder="Last Name" />
            </div>
            <div class="input-wrapper">
              <input type="email" placeholder="Email" />
              <input type="tel" placeholder="Phone/Telegram" />
            </div>
            <div class="input-wrapper select">
              <select class="select">
                <option class="holder" value="" disabled selected>
                  I am interested in
                </option>
                <option value="">Accaunting</option>
                <option value="">IT</option>
                <option value="">Marketing</option>
              </select>
              <select class="select">
                <option class="holder" value="" disabled selected>
                  Select Project Budget in USD
                </option>
                <option value="">100$</option>
                <option value="">500$</option>
                <option value="">1000$</option>
              </select>
            </div>
            <div class="area-wrapper">
              <textarea
                class="area"
                cols="90"
                rows="10"
                placeholder="About your Project"
              ></textarea>
            </div>
            <div class="btn-wrapper">
              <button class="submit" type="submit">Submit</button>
            </div>
          </form>
          <div class="get-touch-contact">
            <div class="contact-infos">
              <h6 class="title">Say Hi</h6>
              <a class="mail" href="#">info@pixyz.com</a>
              <a class="tel" href="#">+998 71 645 57 67</a>
              <a class="telegram" href="#">Telegram</a>
            </div>
            <div class="get-touch-img">
              <img src="@/assets/img/get-touch.png" alt="" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.get-touch {
  padding: 100px 0;

  &-wrapper {
    display: flex;
    flex-direction: column;
    background: #ffffff;
    filter: drop-shadow(3px 3px 30px rgba(0, 0, 0, 0.161));
  }
  .main-wrapper {
    display: flex;
  }
  .get-touch-body {
    display: flex;
    flex-direction: column;
    flex: 1;
    padding: 54px 57px 36px 66px;
    gap: 26px;
  }

  .get-touch-title {
    font-family: "Seg-bold";
    font-size: 40px;
    color: #217a73;
    text-align: start;
  }

  .input-wrapper {
    display: flex;
    align-items: center;
    gap: 30px;

    &.select {
      @include breakpoint(lg) {
        display: flex;
        flex-direction: column;
      }
    }

    .select {
      appearance: none;
      -webkit-appearance: none;
      -moz-appearance: none;
      -ms-appearance: none;
      background-image: url(../assets/img/select-arrow.svg);
      background-repeat: no-repeat;
      background-position: calc(100% - 12px) center !important;
      font-family: "Arial";
      font-size: 16px;
      padding: 18px 55px 20px 28px;
      border: 1px solid #49d6cb;
      width: 100%;
      color: #c9c9c9;

      &:focus {
        outline: none;
      }
    }

    input {
      font-family: "Arial";
      font-size: 16px;
      padding: 18px 0 20px 28px;
      border: 1px solid #49d6cb;
      width: 100%;

      &:focus {
        outline: none !important;
        border: 1px solid #ff8888;
      }

      &::placeholder {
        color: #c9c9c9;
      }
    }
  }

  .area {
    font-family: "Arial";
    font-size: 16px;
    border: 1px solid #49d6cb;
    width: 100%;
    padding: 16px 25px;
    color: #c9c9c9;

    &:focus {
      outline: none !important;
      border: 1px solid #ff8888;
    }

    &::-webkit-input-placeholder {
      color: #c9c9c9;
    }
  }

  .btn-wrapper {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    margin-top: 10px;
  }

  .submit {
    font-family: "Seg";
    font-size: 16px;
    padding: 16px 60px;
    color: #ffffff;
    background: #49d6cb;
    border: 1px solid #49d6cb;
    cursor: pointer;

    &:hover {
      color: #49d6cb;
      background: #ffffff;
    }
  }

  .get-touch-contact {
    display: flex;
    align-items: flex-start;
    min-width: 480px;
    background: #49d6cb;
    position: relative;

    .contact-infos {
      position: absolute;
      top: 16%;
      left: 0;
      display: flex;
      flex-direction: column;
      align-items: flex-end;

      @include breakpoint(lg) {
        position: static;
      }

      a {
        font-family: "Seg";
        text-decoration: none;
        font-size: 16px;
        line-height: 18px;
        color: #ffffff;

        &:not(:last-child) {
          margin-bottom: 60px;
        }

        @include breakpoint(lg) {
          position: absolute;
          margin-bottom: 0 !important;
        }
      }

      .title {
        font-family: "Seg-bold";
        font-size: 32px;
        line-height: 43px;
        color: #ffffff;
        margin-bottom: 45px;
        transform: translateX(20%);
        @include breakpoint(lg) {
          position: absolute;
          bottom: 560px;
          left: 60px;
          transform: translate(0);
          margin-bottom: 0;
        }
      }

      .mail {
        transform: translateX(35%);

        @include breakpoint(lg) {
          bottom: 510px;
          left: 70px;
          transform: translateX(0);
        }
      }

      .tel {
        transform: translateX(45%);
        @include breakpoint(lg) {
          bottom: 440px;
          left: 60px;
          transform: translateX(0);
        }
      }

      .telegram {
        @include breakpoint(lg) {
          bottom: 350px;
          left: 70px;
        }
      }
    }

    .get-touch-img {
      position: absolute;
      bottom: 2%;
      right: 5%;
    }
  }
}
</style>
