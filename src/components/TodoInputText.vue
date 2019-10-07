<template>
    <div>
        <input class="input is-rounded" type="text" :value="value" placeholder="Write what you have to do">
    </div>
  </template>

<script>

export default {
    props: ["value"],
};
</script>

<style>

</style>