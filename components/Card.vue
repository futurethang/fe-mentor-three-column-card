<template>
  <div :class="`card ${position}`" :style="cssVars">
    <img :src="require(`~/assets/${icon}.svg`)" alt="" />
    <h1>{{ headline }}</h1>
    <p>{{ bodyText }}</p>
    <Button :color="this.color" />
  </div>
</template>

<script>
export default {
  props: ["headline", "bodyText", "position", "icon", "color"],
  computed: {
    cssVars() {
      return {
        /* variables you want to pass to css */
        "--color": this.color
      };
    }
  }
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@600&family=Lexend+Deca&display=swap");

.card {
  box-sizing: border-box;
  background-color: var(--color);
  height: 27.5rem;
  width: 20.5rem;
  padding: 2.5rem;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  color: #fff;
  font-family: "Lexend Deca", sans-serif;
}

.card.first {
  border-top-left-radius: 0.5rem;
  border-top-right-radius: 0.5rem;
}
.card.last {
  border-bottom-left-radius: 0.5rem;
  border-bottom-right-radius: 0.5rem;
}

h1 {
  font-family: "Big Shoulders Display", cursive;
  text-transform: uppercase;
  font-size: 2.5rem;
  margin: 1rem 0 0 0;
  color: #fff;
  opacity: 0.9;
}

p {
  color: #fff;
  opacity: 0.6;
  line-height: 1.5rem;
  margin: 0.5rem 0;
}

img {
  width: max-content;
}

@media only screen and (min-width: 768px) {
  .card {
    width: 19rem;
    height: 31.25rem;
  }
  .card.first {
    border-top-left-radius: 0.5rem;
    border-bottom-left-radius: 0.5rem;
    border-top-right-radius: 0;
  }
  .card.last {
    border-bottom-right-radius: 0.5rem;
    border-top-right-radius: 0.5rem;
    border-bottom-left-radius: 0;
  }
}
</style>
