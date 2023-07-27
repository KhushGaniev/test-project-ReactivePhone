<template>
  <div :class="$style.root">
    <div :class="$style.container">
      <div :class="$style.wrapper">
        <div>
          <img :src="require('@/assets/' + image)" alt="icon-card" />
        </div>
        <h2 :class="$style.title">{{ text }}</h2>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "vCard",
  props: {
    image: {
      type: String,
    },
    text: {
      type: String,
    },
  },
};
</script>

<style module>
.container {
  max-width: 360px;
  margin: 0 auto;
}

.wrapper {
  display: flex;
  align-items: center;
  padding: 16px 12px;
  border-radius: 20px;
  border: 1px solid #f3f3f3;
  background: #fff;
}
.title {
  font-size: 16px;
  font-weight: 500;
  line-height: 20px;
  margin-left: 8px;
}
</style>
