<template>
  <div :class="$style.root">
    <div :class="$style.container">
      <vHeader />
      <vCardLearnProgress />
    </div>
  </div>
</template>

<script>
import vHeader from "@/components/vHeader.vue";
import vCardLearnProgress from "@/components/mainLayout/vCardLearnProgress.vue";

export default {
  name: "vMain",
  components: {
    vHeader,
    vCardLearnProgress,
  },
};
</script>

<style module>
.root {
  background: rgba(249, 249, 249, 1);
}
.container {
  max-width: 360px;
  margin: 0 auto;
  padding: 0 16px;
}
</style>
