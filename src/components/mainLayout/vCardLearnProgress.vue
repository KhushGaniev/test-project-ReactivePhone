<template>
  <div :class="$style.root">
    <div :class="$style.container">
      <div :class="$style.wrapper">
        <div :class="$style.learning">
          <div>
            <img src="@/assets/images/hat.svg" alt="icon-hat" />
          </div>
          <div :class="$style.column">
            <div :class="$style.text">
              <h2 :class="$style.title">Learning</h2>
              <p :class="$style.subtitle">Category В</p>
            </div>
            <router-link to="/test" :class="$style.arrow">
              <img src="@/assets/images/chevron.svg" alt="icon-chevron" />
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "vCardLearnProgress",
};
</script>

<style module>
.root {
  margin-top: 8px;
}
.container {
  max-width: 360px;
  margin: 0 auto;
  border-radius: 20px;
  border: 1px solid #f3f3f3;
  background: #fff;
  padding: 24px;
}
.wrapper {
  display: flex;
  flex-direction: column;
}
.title {
  font-size: 20px;
  font-weight: 600;
  line-height: 26px;
}
.subtitle {
  font-size: 14px;
  font-weight: 400;
  line-height: 20px;
  color: rgba(135, 137, 143, 1);
}
.learning {
  display: flex;
}
.column {
  margin-left: 16px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.text {
  display: flex;
  flex-direction: column;
}
.arrow {
  margin-left: 100px;
}
</style>
