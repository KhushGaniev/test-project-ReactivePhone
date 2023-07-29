<template>
  <div :class="$style.root">
    <div :class="$style.container">
      <div :class="$style.wrapper" @click="toggleDone">
        <div :class="$style.done" v-if="count === 1">
          <img src="@/assets/images/done.svg" alt="done-icon" />
        </div>
        <p :class="$style.number">{{ task }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "vCardNumber",
  props: {
    task: {
      type: String,
    },
    count: {
      type: Number,
    },
  },
  methods: {
    toggleDone() {
      this.$emit("update:count", this.count === 0 ? 1 : 0);
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
  position: relative;
  border-radius: 50%;
  width: 71px;
  height: 71px;
  background: white;
  box-shadow: 0px 0px 4px 0px rgba(18, 25, 43, 0.04);
  display: flex;
  justify-content: center;
  cursor: pointer;
}
.number {
  color: #2c2d2e;
  font-size: 18px;
  font-weight: 400;
  line-height: 24px;
  align-self: center;
}
.done {
  position: absolute;
  left: 70%;
}
</style>
