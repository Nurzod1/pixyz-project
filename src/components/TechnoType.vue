<template>
  <div class="techno-type-wrapper">
    <div class="techno-type">
      <img :src="imgUrl" alt="" />
      <span class="name">{{ title }}</span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    imgUrl: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.techno-type-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
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
</style>
