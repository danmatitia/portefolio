<template>
  <div class="formation--row">
      <h2 class="title">
          Formations
      </h2>
      <div class="wrapper--row">
        <formation-card  v-for="(card, index) in three_formation" :info_formation="card" :key="index"/>
    </div>
  </div>

</template>

<script>

import formationCard from './formationCard.vue';

export default {
    name: "formationRow",
    components:  {
        formationCard,
    },
    props: {
        three_formation: Array
    }
}
</script>

<style lang="scss">
    .formation--row{
        .title{
            margin: 60px;
        }
        .wrapper--row{
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin : 40px;
        }
    }
</style>