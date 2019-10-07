<template>
    <div>
        <TodoInputText />
    </div>
</template>

<script>
import TodoInputText from '@/components/TodoInputText.vue';

export default {
    components: {
        TodoInputText,
    },
    data() {
        return {
            todos: ["faire les courses", "promener Béné", "travailler"],
        };
    }
};
</script>

<style>

</style>