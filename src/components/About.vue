<template>
  <div class="about flex-center">
    <div class="main container flex-row-between">
      <section class="section-left">
        <img class="image" src="../images/image.svg" alt="image">
      </section>
      <section class="section-right">
        <p class="subtitle">About Me</p>
        <h1 class="title">Personal Details</h1>
        <p
          class="content"
        >Here, I focus on a range of items and features that we use in life without giving them a second thought. such as Coca Cola. Dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.</p>
        <button>View Full Details</button>
      </section>
    </div>
  </div>
</template>

<script>
export default { name: "About" };
</script>

<style scoped>
.subtitle {
  text-transform: uppercase;
}

.title {
  font-size: calc(35px + 1.5vw);
  line-height: 0.85;
}

section {
  max-width: 500px;
  padding: 20px 0;
}

.section-left {
  padding-right: 25px;
  align-items: center;
}

.section-right {
  padding-left: 25px;
}

img.image {
  width: 500px;
  height: 353px;
  object-fit: cover;
}

@media (max-width: 1000px) {
  .main {
    flex-wrap: wrap;
    text-align: center;
    justify-content: center;
  }

  img.image {
    width: 100%;
    /* height: 100vw; */
  }

  .section-left {
    padding-right: 0;
  }

  .section-right {
    padding-left: 0;
    text-align: center;
  }

  /* button {
    margin: 0 auto;
  } */
}
</style>
