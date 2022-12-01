<template>
  <div class="pixzy-feedback">
    <div class="container">
      <div class="pixzy-feedback-wrapper">
        <h5 class="feedback-title">Customer Testimonials</h5>
        <div class="feedback-body-wrapper">
          <div class="feedback-quote">
            <img src="@/assets/img/quote.png" alt="" />
          </div>
          <div class="feedback-body">
            <p>
              In promotion and advertising, a testimonial or show consists of a
              person's written or spoken statement extolling the virtue of a
              product. The term "testimonial" most commonly applies to the
              sales-pitches attributed to ordinary citizens, whereas the word
              "endorsement" usually applies to pitches by celebrities.
              Testimonials can be part of communal marketing. Sometimes, the
              cartoon character can be a testimonial in a commercial.
            </p>
            <div class="feedback-info">
              <div class="info-img">
                <img src="@/assets/img/woman.jpg" alt="" />
              </div>
              <div class="bio">
                <h6 class="name">Sevara Nazarxon</h6>
                <p class="type">CEO HP Amazon</p>
              </div>
            </div>
          </div>
          <div class="feedback-quote-down">
            <img src="@/assets/img/quote-down.png" alt="" />
          </div>
        </div>
        <div class="dots">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="80"
            height="12"
            viewBox="0 0 80 12"
          >
            <g
              id="Group_571"
              data-name="Group 571"
              transform="translate(-920 -6406)"
            >
              <g
                id="Ellipse_92"
                data-name="Ellipse 92"
                transform="translate(954 6406)"
                fill="#49d6cb"
                stroke="#49d6cb"
                stroke-width="1"
              >
                <circle cx="6" cy="6" r="6" stroke="none" />
                <circle cx="6" cy="6" r="5.5" fill="none" />
              </g>
              <g
                id="Ellipse_95"
                data-name="Ellipse 95"
                transform="translate(976 6408)"
                fill="#fff"
                stroke="#49d6cb"
                stroke-width="1"
              >
                <circle cx="4" cy="4" r="4" stroke="none" />
                <circle cx="4" cy="4" r="3.5" fill="none" />
              </g>
              <g
                id="Ellipse_96"
                data-name="Ellipse 96"
                transform="translate(992 6408)"
                fill="#fff"
                stroke="#49d6cb"
                stroke-width="1"
              >
                <circle cx="4" cy="4" r="4" stroke="none" />
                <circle cx="4" cy="4" r="3.5" fill="none" />
              </g>
              <g
                id="Ellipse_93"
                data-name="Ellipse 93"
                transform="translate(920 6408)"
                fill="#fff"
                stroke="#49d6cb"
                stroke-width="1"
              >
                <circle cx="4" cy="4" r="4" stroke="none" />
                <circle cx="4" cy="4" r="3.5" fill="none" />
              </g>
              <g
                id="Ellipse_94"
                data-name="Ellipse 94"
                transform="translate(936 6408)"
                fill="#fff"
                stroke="#49d6cb"
                stroke-width="1"
              >
                <circle cx="4" cy="4" r="4" stroke="none" />
                <circle cx="4" cy="4" r="3.5" fill="none" />
              </g>
            </g>
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
.pixzy-feedback {
  padding: 76px 0 81px 0;
  background: #f4f6fc;

  .feedback-body-wrapper {
    position: relative;
    margin-bottom: 41px;
  }

  .feedback-quote {
    position: absolute;
    top: -50px;
    left: 15%;
  }

  .feedback-quote-down {
    position: absolute;
    right: 20%;
    bottom: 50px;
  }

  .feedback-title {
    font-family: "Seg-bold";
    font-size: 40px;
    color: #217a73;
    text-align: center;
    margin-bottom: 51px;
  }

  .feedback-body {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 50px;

    p {
      font-family: "Seg";
      font-size: 24px;
      line-height: 32px;
      color: #7d7d7d;
      text-align: center;
      width: 50%;
    }
  }

  .feedback-info {
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .info-img {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    overflow: hidden;

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }

  .bio {
    display: flex;
    flex-direction: column;

    .name {
      font-family: "Seg-bold";
      font-size: 16px;
      color: #49d6cb;
    }

    .type {
      font-family: "Seg";
      font-size: 16px;
      color: #000000;
      white-space: nowrap;
    }
  }

  .dots {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>
