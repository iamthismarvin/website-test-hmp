<template>
  <div class="gallery flex-center">
    <div class="main container">
      <div class="photos flex-row-around">
        <div class="pictures" v-for="{id, src, alt} in pictures" :key="id">
          <a :href="require(`../images/${src}`)" target="blank" rel="noreferrer">
            <img class="picture" :src="require(`../images/${src}`)" :alt="alt">
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Gallery",
  data: () => ({
    pictures: [
      { id: 0, src: "image.svg", alt: "picture_0" },
      { id: 1, src: "image.svg", alt: "picture_1" },
      { id: 2, src: "image.svg", alt: "picture_2" },
      { id: 3, src: "image.svg", alt: "picture_3" }
    ]
  })
};
</script>

<style scoped>
.title,
.description {
  text-align: center;
  color: #fff;
}

.gallery {
  background-image: linear-gradient(to right, #8490ff 0%, #62bdfc 100%);
  min-height: 230px;
  align-items: center;
  color: #fff;
}

.photos {
  flex-wrap: wrap;
}

img.picture {
  width: 200px;
  height: 200px;
  object-fit: cover;
  margin: 15px;
}
</style>
