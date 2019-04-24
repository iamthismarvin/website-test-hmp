<template>
  <header class="navigation flex-center">
    <div class="main container flex-row-between">
      <img
        class="logo"
        src="../images/logo.svg"
        alt="logo"
        v-on:click="toggleStatus = !toggleStatus"
      >
      <div class="desktop">
        <ul class="links">
          <li class="link" v-for="{id, name, path} in pages" :key="id">
            <a :href="path">{{name}}</a>
          </li>
        </ul>
      </div>
      <div class="mobile" v-if="toggleStatus">
        <ul class="links">
          <li class="link" v-for="{id, name, path} in pages" :key="id">
            <a :href="path">{{name}}</a>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script>
import { pages } from "~/data/pages.json";

export default {
  name: "Navigation",
  data: () => ({ pages, toggleStatus: false })
};
</script>

<style scoped>
.main {
  align-items: center;
}

img.logo {
  width: 50px;
  height: 50px;
  object-fit: cover;
}

.links {
  display: flex;
  flex-direction: row;
  justify-content: right;
  padding: 0;
}

.links li {
  list-style: none;
  padding: 0;
  text-align: center;
}

.links li > a {
  color: #222;
  text-decoration: none;
  text-transform: uppercase;
  padding: 0 10px;
}

.mobile {
  display: none;
}

@media (max-width: 800px) {
  .desktop {
    display: none;
  }
  .mobile {
    display: block;
  }

  .main {
    flex-direction: column;
  }

  .links {
    flex-direction: column;
  }

  img.logo {
    cursor: pointer;
  }

  .links li {
    display: block;
    width: 70vw;
    font-size: 1.5em;
    background-image: linear-gradient(
      to right,
      #8490ff 0%,
      #6bb2fd 50%,
      #62bdfc 100%
    );
  }

  .links li > a {
    text-transform: none;
    color: #fff;
  }
}
</style>