<template>
  <div class="layout">
    <Navigation/>
    <slot/>
    <Footer/>
  </div>
</template>

<script>
import Navigation from "~/components/Navigation.vue";
import Footer from "~/components/Footer.vue";

export default {
  components: {
    Navigation,
    Footer
  }
};
</script>


<style>
html {
  margin: 0;
  padding: 0;
}

body {
  font-family: "Segoe UI", sans-serif;
  color: #222;
  margin: 0;
  padding: 0;
  line-height: 1.5;
}

p {
  color: #777;
}

.layout {
  max-width: 100%;
  margin: 0 auto;
}

/* Child-Component CSS */
.flex-center {
  display: flex;
  justify-content: center;
}

.flex-row-between {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.flex-row-around {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}

.container {
  width: 1200px;
  padding: 20px;
  margin: 0;
}

button {
  background-image: linear-gradient(
    to right,
    #8490ff 0%,
    #6bb2fd 50%,
    #62bdfc 100%
  );
  height: 45px;
  width: 173px;
  border: solid 1px #707070;
  color: #fff;
  text-transform: uppercase;
  font-size: 14px;
  cursor: pointer;
}
</style>
