<template>

    <section>
        <h1 class="title text-center">liste des chiens</h1>

        <Tabledog :dogs="dogs" v-on:action2="dog => delet(dog)"> </Tabledog>

        <Adddog v-on:action1="dog => adddog(dog)"> </Adddog>
         
    </section>

</template>

<script>

import Tabledog from './Tabledog.vue';
import Adddog from './Adddog.vue';

export default {
    name: 'gestiondog',
    components: {
        Tabledog,
        Adddog,
    }, 
    data:  function () {
        return {
            dogs: [
                {'id': 0, 'name': 'fido', 'race': 'corgi', 'birthdate': '09/02/2017'},
                {'id': 1, 'name': 'rex', 'race': 'dhalmacien', 'birthdate': '03/07/2017'},
                {'id': 2, 'name': 'milou', 'race': 'berger', 'birthdate': '03/06/2017'}
            ]
        };
    },
    methods: {
        adddog(dog) {
            dog.id = this.dogs.length;
            this.dogs.push(dog);
        },
        delet(dog) {
            this.dogs.splice(this.dogs.indexOf(dog), 1);
        }
    },
}
</script>

<style>

</style>
