<template>
  <div class="projects flex-center">
    <div class="main container flex-center">
      <h1 class="title">Our Latest Featured Projects</h1>
      <p class="description">Who are in extremely love with eco friendly system.</p>
      <ul class="filters">
        <li class="filter" v-for="{id, tag, link} in filters" :key="id">
          <a :href="link" v-on:click="filterEvent">{{tag}}</a>
        </li>
      </ul>
      <div class="projects flex-row-around">
        <div class="project" v-for="{id, title, tag, thumbnail} in projects" :key="id">
          <img class="thumbnail" :src="require(`../images/${thumbnail}`)" :alt="title">
          <h3>{{title}}</h3>
          <p>{{tag}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Projects",
  data: () => ({
    filters: [
      { id: 0, tag: "All", link: "/" },
      { id: 1, tag: "Vector", link: "/" },
      { id: 2, tag: "Raster", link: "/" },
      { id: 3, tag: "UI/UX", link: "/" },
      { id: 4, tag: "Printing", link: "/" }
    ],
    projects: [
      {
        id: 0,
        title: "2D Vinyl Design",
        tag: "Vector",
        thumbnail: "image.svg"
      },
      {
        id: 1,
        title: "2D Vinyl Design",
        tag: "Vector",
        thumbnail: "image.svg"
      },
      {
        id: 2,
        title: "Creative Poster Design",
        tag: "Agency",
        thumbnail: "image.svg"
      },
      {
        id: 3,
        title: "Embosed Logo Design",
        tag: "Portal",
        thumbnail: "image.svg"
      },
      {
        id: 4,
        title: "3D Helmet Design",
        tag: "Vector",
        thumbnail: "image.svg"
      },
      {
        id: 5,
        title: "2D Vinyl Design",
        tag: "Raster",
        thumbnail: "image.svg"
      }
    ]
  }),
  // Work on filter functionality.
  methods: {
    filterEvent: () => {
      alert("You clicked the " + " filter.");
      preventDefault();
    }
  }
};
</script>

<style scoped>
.main {
  flex-direction: column;
  text-align: center;
}

.projects {
  flex-wrap: wrap;
}

.filters {
  display: flex;
  flex-direction: row;
  justify-content: center;
  padding: 0;
  flex-wrap: wrap;
}

.filters li {
  list-style: none;
  padding: 0;
}

.filters li > a {
  color: #777;
  text-decoration: none;
  text-transform: uppercase;
  padding: 0 10px;
}

img.thumbnail {
  width: 370px;
  height: 276px;
  object-fit: cover;
  margin: 15px;
}

@media (max-width: 800px) {
  img.thumbnail {
    width: 250px;
    height: 156px;
  }
}
</style>
