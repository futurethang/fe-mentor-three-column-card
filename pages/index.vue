<template>
  <div class="container">
    <div class="wrapper">
      <Card
        position="first"
        icon="icon-sedans"
        headline="Sedans"
        bodyText="Choose a sedan for its affordability and excellent fuel economy.
      Ideal for cruising in the city or on your next road trip."
        color="hsl(31, 77%, 52%)"
      >
      </Card>
      <Card
        position="mid"
        icon="icon-suvs"
        headline="SUVs"
        bodyText="Take an SUV for its spacious interior, power, and versatility.
      Perfect for your next family vacation and off-road adventures."
        color="hsl(184, 100%, 22%)"
      >
      </Card>
      <Card
        position="last"
        icon="icon-luxury"
        headline="Luxury"
        bodyText="Cruise in the best car brands without the bloated prices. Enjoy the
      enhanced comfort of a luxury rental and arrive in style."
        color="hsl(179, 100%, 13%)"
      >
      </Card>
    </div>
    <footer class="attribution">
      Challenge by
      <a href="https://www.frontendmentor.io?ref=challenge" target="_blank"
        >Frontend Mentor</a
      >. Coded by <a href="https://kevin-hyde.netlify.app/" target="blank">Kevin Hyde</a>.
    </footer>
  </div>
</template>

<script>
import Card from "../components/Card.vue";
export default {
  components: { Card }
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 2rem;
}
.wrapper {
  display: flex;
  flex-direction: column;
}

.attribution {
  margin-top: 2rem;
  text-align: center;
  font-size: 0.75rem;
}

@media only screen and (min-width: 768px) {
  .container {
    height: 88vh;
  }
  .wrapper {
    flex-direction: row;
  }
}
</style>
