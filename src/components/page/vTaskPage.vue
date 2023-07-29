<template>
  <div :class="$style.root">
    <div :class="$style.container">
      <div :class="$style.wrapper">
        <div @click="$router.push('/')" :class="$style.exit">
          <div>
            <img src="@/assets/images/arrowLeft.svg" alt="arrow-icon" />
          </div>
          <p :class="$style.exitText">Learning</p>
        </div>
        <h2 :class="$style.title">Tests</h2>
        <hr :class="$style.line" />
        <vCardNumberItems />
      </div>
    </div>
  </div>
</template>

<script>
import vCardNumberItems from "@/components/taskLayout/vCardNumberItems";

export default {
  name: "vTaskLayout",
  components: {
    vCardNumberItems,
  },
};
</script>

<style module>
.root {
  background: rgba(249, 249, 249, 1);
  padding-top: 62px;
}
.container {
  max-width: 360px;
  margin: 0 auto;
}
.exit {
  display: flex;
  align-items: center;
  cursor: pointer;
  margin-bottom: 30px;
}
.exitText {
  margin-left: 15px;
  color: #2c2d2e;
  font-size: 18px;
  font-weight: 500;
  line-height: 26px;
}
.title {
  text-align: center;
  color: #ff7355;
  font-size: 14px;
  font-weight: 500;
  line-height: 20px;
}
.line {
  position: relative;
  width: 109px;
  height: 2px;
  background: #ff7355;
  top: 14px;
  left: 50%;
  transform: translateX(-50%);
}
</style>
