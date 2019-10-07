<template>
    <div>
        <input class="input is-rounded" 
        type="text"
        placeholder="Write what you have to do"
        :value="value"
        v-on="listeners" />
    </div>
  </template>

<script>

export default {
    props: ["value"],
   computed: {
    listeners() {
      return {
        // Pass all component listeners directly to input
        ...this.$listeners,
        // Override input listener to work with v-model
        input: event => this.$emit("input", event.target.value)
      };
    }
  }
};
</script>

<style>

</style>