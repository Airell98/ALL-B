<template>
  <div>
    <div class="hero-image">
      <div style="height: 200px;"></div>
      <div class="hero-text">
        <h1>All-B</h1>
        <p>Providing solutions through technology</p>

        <div style="height: 250px;"></div>
      </div>
    </div>
    <div style="height: 50px;"></div>
    <HomeMiddle/>
  </div>
</template>

<script>
import HomeMiddle from "../components/HomeMiddle.vue";
export default {
  components: {
    HomeMiddle,
  },
};
</script>

<style lang="scss" scoped>
.hero-image {
  /* Use "linear-gradient" to add a darken background effect to the image (photographer.jpg). This will make the text easier to read */
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url("https://images.unsplash.com/photo-1510511459019-5dda7724fd87?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80");
  width: 100%;
  margin: auto;
  /* Set a specific height */
  height: 100%;

  /* Position and center the image to scale nicely on all screens */
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  .hero-text {
    text-align: center;
    h1 {
      font-size: 90px;
      letter-spacing: 5px;
      font-family: "Tienne", serif;
    }
    p {
      font-size: 25px;
      font-family: "Recursive", sans-serif;
    }
    // position: absolute;
    // top: 50%;
    // left: 50%;

    color: rgb(231, 225, 225);
  }
}
</style>
