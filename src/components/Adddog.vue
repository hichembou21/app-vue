<template>
    <form v-on:submit.prevent="onSubmit">
        <fieldset class="form-group">
        <input type="text" name="name" v-model="dog.name">
        <input type="text" name="race" v-model="dog.race">
        <input type="date" name="birthdate" v-model="dog.birthdate">
        <input type="submit" value="Add" @click="action1()">
        </fieldset>
    </form>
</template>

<script>
export default {
    name: 'adddog',
    data: function () {
        return {
            dog: {
                name: '',
                race: '',
                birthdate: ''
            }
        };
    },
    methods: {
      action1() { 
          this.$emit('action1', Object.assign({}, this.dog));
      },
  }
}
</script>

<style>

</style>
