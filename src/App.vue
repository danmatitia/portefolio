<template>
  <div id="app">
    <nav id="nav">
      <ul>
        <li><router-link to="/">Accueil</router-link></li>
        <li><router-link to="/profile">About</router-link></li>
        <li>
          <a to="/" v-on:click="email()">
            <span class="email">Contact</span></a>
        </li>
      </ul>
    </nav>
    <formationCard/>
    
  </div>
</template>

<script>
import formationCard from '../src/components/formationCard.vue'

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
body {
  background-color: #d6dfe2;
}
#logo {
  width: 56%;
  max-width: 100%;
}
#navlogo {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background-color: #31bcc6;
  margin: -10px -10px 0px -10px;
  height: 115px;
}
nav {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background-color: #f7f475;
  margin: 0px -10px 0px -10px;
  height: 50px;
}
nav li {
  display: inline-block;
  margin: 0 8px;
}
.email {
  color: rgb(38, 42, 248);
  cursor: pointer;
}

</style>
