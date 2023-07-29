<template>
  <div :class="$style.root">
    <div :class="$style.container">
      <div :class="$style.wrapper">
        <vCardNumber />
        <vCardNumber />
        <vCardNumber />
        <vCardNumber />
        <vCardNumber />
        <vCardNumber />
      </div>
    </div>
  </div>
</template>

<script>
import vCardNumber from "@/components/taskLayout/vCardNumber";

export default {
  name: "vCardNumberItems",
  components: {
    vCardNumber,
  },
};
</script>

<style module>
.root {
  padding-top: 45px;
}
.container {
  max-width: 360px;
  margin: 0 auto;
}
.wrapper {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 15px;
}
</style>
