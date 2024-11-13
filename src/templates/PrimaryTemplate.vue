<script setup>
defineProps({
  headerImg: {
    type: String,
    required: true
  }
})
import Alien from "../vues/Alien.vue";
</script>

<template>
  <section class="primary-template">
    <header>
      <div class="header-img" :style="'background-image: url(../src/assets/' + headerImg + ');'">
        Virtual Voyage Redux
      </div>

      <nav>
        <router-link :to="{ name: 'Home' }">Home</router-link>
        <router-link :to="{ name: 'Alien'}">Alien</router-link>
        <router-link :to="{ name: 'About' }">About</router-link>
      </nav>
    </header>


    <section class="main">
      <slot>Welcome to my site!</slot>
    </section>

    <footer>
      <div class="back-to-top">go to top of page</div>
      <div class="copyright">This Year</div>
    </footer>
  </section>
</template>

<style scoped>
/*Mobile First*/
section.primary-template {
  h1 {
    color: white;
  }

  header {
    div.header-img {
      border: 1px solid white;
      background-repeat: repeat-x;
      background-size: contain;
      background-position: center center;
      min-height: 35vh;
    }
  }

  nav.top {
    background-color: white;
    text-align: left;
    height: auto;

    img {
      width: 100%;
      height: auto;
      margin: 0;
      padding: 0;
    }

    .items {
      display: flex;
      justify-content: space-between;

      a {
        text-transform: uppercase;
        color: white;
        text-decoration: none;
      }

      a:hover {
        color: white;
        font-weight: bold;
      }
    }
  }

  section.main {
    max-width: 800px;
    margin: 0 auto;
    border: 1px solid red;
    padding: 1rem;
  }
}

header, footer {
  background-color: black;
  color: white;
}
</style>