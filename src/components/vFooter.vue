<template>
  <div :class="$style.root">
    <div :class="$style.container">
      <div :class="$style.wrapper">
        <button :class="$style.home">
          <div>
            <img
              src="@/assets/images/iconsFooter/home.svg"
              alt="icon-home"
              :class="[{ [$style.img]: $route.name === 'home' }]"
            />
          </div>
          <h4
            :class="[$style.text, { [$style.active]: $route.name === 'home' }]"
          >
            Home
          </h4>
        </button>
        <button :class="$style.plan">
          <div>
            <img src="@/assets/images/iconsFooter/route.svg" alt="icon-home" />
          </div>
          <h4
            :class="[$style.text, { [$style.active]: $route.name === 'plan' }]"
          >
            Your plan
          </h4>
        </button>
        <button :class="$style.leaderboard">
          <div>
            <img
              src="@/assets/images/iconsFooter/ranking.svg"
              alt="icon-home"
            />
          </div>
          <h4
            :class="[
              $style.text,
              { [$style.active]: $route.name === 'leaderboard' },
            ]"
          >
            Leaderboard
          </h4>
        </button>
        <button :class="$style.profile">
          <div>
            <img
              src="@/assets/images/iconsFooter/profile.svg"
              alt="icon-home"
            />
          </div>
          <h4
            :class="[
              $style.text,
              { [$style.active]: $route.name === 'profile' },
            ]"
          >
            Profile
          </h4>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "vFooter",
};
</script>

<style module>
.root {
  margin-top: 70px;
}
.container {
  max-width: 360px;
  margin: 0 auto;
  padding: 0 16px;
}
.wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.text {
  margin-top: 12px;
  font-size: 12px;
  font-weight: 500;
  line-height: 14px;
}
.img {
  padding: 5px;
  border-radius: 12px;
  background: #ffe3dd;
  margin-bottom: -5px;
}
.active {
  color: rgba(255, 115, 85, 1);
}
</style>
