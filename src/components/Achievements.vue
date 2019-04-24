<template>
  <div class="achievements flex-center">
    <div class="main container flex-row-between">
      <div class="list" v-for="{id, title, count} in achievements" :key="id">
        <h1>{{count}}</h1>
        <p class="achievement-title">{{title}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Achievements",
  data: () => ({
    achievements: [
      { id: 0, title: "Projects Completed", count: 6598 },
      { id: 1, title: "Happy Clients", count: 6598 },
      { id: 2, title: "Cups of Coffee", count: 9235 },
      { id: 3, title: "Real Professionals", count: 6598 }
    ]
  })
};
</script>

<style scoped>
.achievements {
  background-image: linear-gradient(to right, #8490ff 0%, #62bdfc 100%);
  min-height: 320px;
  align-items: center;
}

.main {
  color: #fff;
  flex-wrap: wrap;
}

.list {
  text-align: center;
}

.achievement-title {
  /* font-size: 12px; */
  color: #fff;
}

@media (max-width: 800px) {
  .main {
    flex-direction: column;
  }
}
</style>
