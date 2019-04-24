<template>
  <div class="showcase flex-center">
    <div class="main container flex-row-between">
      <section class="section-left">
        <!-- <h3>This is me!</h3> -->
        <h1 class="big-font">PEPE GARCIA</h1>
        <p
          class="description"
        >You will begin to realise why this exercise is called the Dickens Pattern with reference to the ghost show Scrooge some different futures.</p>
        <button>Discover Now</button>
      </section>
      <section class="section-right">
        <img class="image" src="../images/image.svg" alt="image">
      </section>
    </div>
  </div>
</template>

<script>
export default { name: "Showcase" };
</script>

<style scoped>
.showcase {
  background-color: #f9f9ff;
}

section {
  max-width: 500px;
  padding: 20px 0;
}

.section-left {
  padding-right: 25px;
}

.section-right {
  display: flex;
  justify-content: right;
  padding-left: 25px;
}

.big-font {
  font-weight: normal;
  font-size: calc(50px + 1.5vw);
  line-height: 0.85;
}

img.image {
  width: 500px;
  height: 585px;
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
    height: 400px;
  }

  .section-left {
    padding-right: 0;
  }

  .section-right {
    padding-left: 0;
  }
}
</style>
