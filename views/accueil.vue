<template>
   <div class="accueil">
    <formationRow />
  </div>
</template>

<script>
//import
import BDD from '../src/BDD'

//Compenents    
import formationRow from '../src/components/formationRow.vue'
export default {
    name: 'Accueil',
    components: {
        formationRow
    },
    setup() {
        class formation {
            constructor(name,image,description,time){
                this.name = name
                this.image = image
                this.description = description
                this.time = time
            }
        }
        console.log(BDD),
        console.log(formation)
    }
}
</script>

<style>

</style>