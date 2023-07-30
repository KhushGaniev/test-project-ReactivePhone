<template>
  <div :class="$style.root">
    <div :class="$style.container">
      <div :class="$style.wrapper">
        <div :class="$style.card" v-for="item in arrCard" :key="item.id">
          <div>
            <img :src="require('@/assets/' + item.image)" alt="icon-card" />
          </div>
          <p :class="$style.text">{{ item.text }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "vShapeCard",
  data() {
    return {
      arrCard: [
        { id: 1, text: "Mistakes", image: "images/pen.svg" },
        { id: 1, text: "Statistics", image: "images/chartBar.svg" },
        { id: 1, text: "Highway Code", image: "images/book.svg" },
        { id: 1, text: "Favorites", image: "images/bookmarks.svg" },
      ],
    };
  },
};
</script>

<style module>
.root {
  margin-top: 25px;
}
.container {
  max-width: 360px;
  margin: 0 auto;
  padding: 0 16px;
}
.wrapper {
  display: flex;
  justify-content: space-between;
}
.card {
  display: flex;
  flex-direction: column;
}
.text {
  margin: 8px 0px 0px 5px;
  max-width: 30px;
  font-size: 14px;
  font-weight: 400;
  line-height: 20px;
}
</style>
