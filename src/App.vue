<template>
  <div id="app">
    <formationCard/>
    <p slt class="slt">slt</p>
  </div>
</template>

<script>
import formationCard from './components/formationCard.vue'

export default {
  name: 'App',
  components: {
    formationCard
  }
}
</script>

<style lang="scss">
  @import url("../style/reset.css");
  @import url("https://fonts.googleapis.com/css2?family=Roboto%3Awght%40300%3B400%3B700&display=swap");
#app {
  font-family: 'Roboto', sans-serif;

}
</style>
