<template>
  <div class="services flex-center">
    <div class="main container flex-center">
      <h1 class="title">My Offered Services</h1>
      <p
        class="description"
      >At about this time of year, some months after New Year’s resolutions have been made and kept, or made and neglected.</p>
      <div class="services flex-row-around">
        <div class="service" v-for="{id, title, description, thumbnail} in services" :key="id">
          <img class="thumbnail" :src="require(`../images/${thumbnail}`)" :alt="title">
          <h3>{{title}}</h3>
          <p>{{description}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Services",
  data: () => ({
    services: [
      {
        id: 0,
        title: "Web Design",
        description:
          "“It is not because things are difficult that we do not dare; it is because we do not dare that they are difficult.”",
        thumbnail: "image.svg"
      },
      {
        id: 1,
        title: "Web Development",
        description:
          "If you are an entrepreneur, you know that your success cannot depend on the opinions of others. Like the wind, opinions.",
        thumbnail: "image.svg"
      },
      {
        id: 2,
        title: "Photography",
        description:
          "Do you want to be even more successful? Learn to love learning and growth. The more effort you put into improving your skills.",
        thumbnail: "image.svg"
      },
      {
        id: 3,
        title: "Clipping Path",
        description:
          "Hypnosis quit smoking methods maintain caused quite a stir in the medical world over the last two decades. There is a lot of argument.",
        thumbnail: "image.svg"
      },
      {
        id: 4,
        title: "Apps Interface",
        description:
          "Do you sometimes have the feeling that you’re running into the same obstacles over and over again? Many of my conflicts.",
        thumbnail: "image.svg"
      },
      {
        id: 5,
        title: "Graphic Design",
        description:
          "You’ve heard the expression, “Just believe it and it will come.” Well, technically, that is true, however, ‘believing’ is not just thinking that.",
        thumbnail: "image.svg"
      }
    ]
  })
};
</script>

<style scoped>
.main {
  flex-direction: column;
  text-align: center;
}

.services {
  flex-wrap: wrap;
}

.service {
  max-width: 373px;
  margin: 20px 10px;
}

img.thumbnail {
  width: 80px;
  height: 50px;
  object-fit: cover;
  margin: 15px;
}
</style>
