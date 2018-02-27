<template>
    <section>
        <img src="../assets/simplon.png" alt="logo simplon" width="400" height="300" @click="show()">
        <div>
        <input type="number" v-model.number="variable1">
        <select name="operator">
            <option value="plus">+</option>
            <option value="moins">-</option>
            <option value="multi">*</option>
            
        </select>
        <input type="number" v-model.number="variable2">
        <p v-if="variable1 && variable2"> {{variable1}} +  {{variable2}} = {{ variable1 + variable2 }} </p>        
        </div>
        <ul>
            <li v-for="(item, index) of tab" :key="index" @click="showItem(item)" @dblclick="deleteItem(item)"> 
               {{index}} {{item}}
            </li>
        </ul>
        <!-- <a v-bind:href="variable1">bloup</a> v-bind:href pour associé des variables à des attributs -->
    </section>
  
</template>

<script>
export default {
    name: 'first',
    data: function () {
        return {
            variable1: 0,
            variable2: 0,
            tab: ['ga', 'zo', 'bu', 'meu']
        };
    },
    methods: {
        show() {
            alert('hello simplon');
        }, 
        showItem(item) {
            console.log(item);
        },
        deleteItem(item) {
            this.tab.splice(this.tab.indexOf(item) , 1);
        }
    }
}
</script>



<style>

</style>
