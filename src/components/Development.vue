<template>
  <div class="development">
    <div class="development-type">
      <div class="development-header" @click="isActive = !isActive">
        <h6>{{ title }}</h6>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="27.001"
          height="15.622"
          viewBox="0 0 27.001 15.622"
        >
          <g
            id="Group_1048"
            data-name="Group 1048"
            transform="translate(-1480.379 -2194.379)"
          >
            <line
              id="Line_10"
              data-name="Line 10"
              x2="11.379"
              y2="11.379"
              transform="translate(1482.5 2196.5)"
              fill="none"
              stroke="#fff"
              stroke-linecap="round"
              stroke-width="3"
            />
            <line
              id="Line_11"
              data-name="Line 11"
              x1="11.379"
              y2="11.379"
              transform="translate(1493.879 2196.5)"
              fill="none"
              stroke="#fff"
              stroke-linecap="round"
              stroke-width="3"
            />
          </g>
        </svg>
      </div>
      <div class="content-wrapper" v-if="isActive">
        <slot />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive: false,
    };
  },
  props: {
    title: {
      type: String,
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.development {
  &-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 14px 29px 18px 32px;
    background: #00a49a;
    border-radius: 15px;
    margin-bottom: 8px;
    cursor: pointer;

    h6 {
      font-family: "Seg-bold";
      font-size: 24px;
      line-height: 32px;
      color: #ffffff;
    }
  }

  .content-wrapper {
    padding: 32px 0;
  }
}
</style>
