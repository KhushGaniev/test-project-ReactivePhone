<template>
  <div :class="$style.root">
    <div :class="$style.container">
      <div :class="$style.wrapper" @click="toggleDone">
        <div :class="$style.done" v-if="showDone">
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
    id: {
      type: Number,
    },
    task: {
      type: String,
    },
  },
  data() {
    return {
      showDone: false, // По умолчанию блок скрыт
    };
  },
  methods: {
    toggleDone() {
      this.showDone = !this.showDone; // Переключаем состояние блока при клике
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
