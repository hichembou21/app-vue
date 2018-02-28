<template>
    <ul>
        <li v-for="(item, index) of tab" :key="index"
        @click="action1(item)" @dblclick="action2(item)"> 
            {{index}} {{item}}
        </li>
    </ul>
</template>

<script>
export default {
  name: "list",
  props: {
      tab: {
          type:Array,
          required: true
      }
  },
  methods: {
      action1(item) {
          this.$emit('action1', item);
      },
      action2(index) {
          this.$emit('action2', index);          
      }
  }
};
</script>

<style>

</style>
