<template>
    <table class="table">
        <thead class="thead-dark">
            <th scope="col">id</th>
            <th scope="col">name</th>
            <th scope="col">race</th>
            <th scope="col">birthdate</th> 
            <th scope="col">ops</th>     
        </thead>
        <tbody>
        <tr v-for="dog of dogs" :key="dog.id"> 
            <td>{{dog.id}}</td>
            <td>{{dog.name}}</td>  
            <td>{{dog.race}}</td>  
            <td>{{dog.birthdate}}</td> 
            <button @click="action2(dog)">delete</button>           
        </tr>
        </tbody>
    </table>
</template>

<script>
export default {
    name: 'tabledog',
    props: {
      dogs: {
          type:Array,
          required: true
      }
    },
    methods: {
      action2(dog) { 
          this.$emit('action2', dog);
      }
    }
}
</script>

<style>

</style>
