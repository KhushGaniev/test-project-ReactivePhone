<template>
  <header :class="$style.root">
    <div :class="$style.container">
      <div :class="$style.wrapper">
        <h1 :class="$style.title">Ray Driving Theory</h1>
        <div :class="$style.icons">
          <div :class="$style.iconCrown">
            <img src="@/assets/images/crown.svg" alt="icon-crown" />
          </div>
          <div :class="$style.iconFire">
            <img src="@/assets/images/fire.svg" alt="icon-crown" />
            <p :class="$style.numberFire">13</p>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "vHeader",
};
</script>

<style module>
.root {
  padding: 48px 0 8px 0;
}
.container {
  max-width: 360px;
  margin: 0 auto;
}
.title {
  font-weight: 500;
  line-height: 26px;
  font-size: 18px;
}
.wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.icons {
  display: flex;
}
.iconCrown {
  padding: 8px;
  background-color: white;
  border-radius: 8px;
}
.iconFire {
  display: flex;
  align-items: center;
  margin-left: 8px;
  padding: 8px;
  background-color: white;
  border-radius: 8px;
  width: 60px;
}
.numberFire {
  font-size: 14px;
  font-weight: 500;
  line-height: 20px;
}
</style>
