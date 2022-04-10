<template>
   <div class="accueil">
    <formationRow v-for="(card, i) in data_formation" :key="i" :three_formation="data"/>
  </div>
</template>

<script>
//import
import BDD from '../src/BDD'
import { onMounted, ref } from 'vue'
//Compenents    
import formationRow from '../src/components/formationRow.vue'
export default {
    name: 'Accueil',
    components: {
        formationRow,
    },
    setup() {
        class Formation {
            constructor(name,image,description,time){
                this.name = name
                this.image = image
                this.description = description
                this.time = time
            }
        }
        let data_formation = ref([]);

        const makeDataFormation = () => {
            let three_formation = []

            for (const formation of BDD) {
                const new_formation = new Formation(formation.name, formation.image, formation.description, formation.time)
                if (three_formation.length === 2) {
                    three_formation.push(new_formation);
                    data_formation.value.push(three_formation);
                    three_formation = [];
                } else {
                    three_formation.push(new_formation);
                }
            }
        }
        onMounted(makeDataFormation);
    }
}
</script>

<style>

</style>