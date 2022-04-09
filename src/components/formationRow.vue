<template>
  <div class="formation--row">
      <h2 class="title">
          Formations
      </h2>
      <formationCard/>
  </div>

</template>

<script>

import formationCard from './formationCard.vue';

export default {
    name: "formationRow",
    components:  {
        formationCard
    }
}
</script>

<style>

</style>