<template>
  <div :class="$style.root">
    <div :class="$style.container">
      <div :class="$style.wrapper">
        <p :class="$style.number">1</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "vCardNumber",
};
</script>

<style module>
.container {
  max-width: 360px;
  margin: 0 auto;
}
.wrapper {
  border-radius: 50%;
  width: 71px;
  height: 71px;
  box-shadow: 0px 0px 4px 0px rgba(18, 25, 43, 0.04);
  display: flex;
  justify-content: center;
}
.number {
  color: var(--light-text-color-text-primary, #2c2d2e);
  font-size: 18px;
  font-weight: 400;
  line-height: 24px;
  align-self: center;
}
</style>
