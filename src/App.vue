<script setup>
import HelloWorld from './components/HelloWorld.vue'
import PointPlacer from 'vue-plotting-ui-lib'
import "vue-plotting-ui-lib/style.css"

const measurements = [
  { y: 2, color: "blue" }, { y: 57, color: "red" },
  { y: 491, color: "green" }, { y: 667, color: "yellow" }
]

</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
<PointPlacer image-source="https://furtadosbeta.gumlet.io/media/catalog/product/2/0/208079_1_1.jpg"
    :measurements="measurements" :on-save-click="(lines) => console.log(lines)" />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
