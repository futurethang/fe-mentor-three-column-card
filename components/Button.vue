<template>
  <button>Learn More</button>
</template>

<script>
export default {
  props: ["color"],
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
button {
  box-sizing: border-box;
  border: none;
  border-radius: 4rem;
  padding: 0 1.75rem;
  width: 9rem;
  height: 3rem;
  background-color: #fff;
  color: var(--color);
  font-size: 0.95rem;
  font-family: "Lexend Deca";
}

button:hover {
  background-color: var(--color);
  border: 2px solid white;
  color: white;
  cursor: pointer;
}
</style>
