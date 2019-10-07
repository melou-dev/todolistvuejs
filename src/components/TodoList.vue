<template>
    <div>
        <TodoInputText v-model="newTodoText" />
        <TodoListItem :todos="todos" />
    </div>
</template>

<script>
import TodoInputText from '@/components/TodoInputText.vue';
import TodoListItem from '@/components/TodoListItem.vue';

export default {
    components: {
        TodoInputText,
        TodoListItem,
    },
    data() {
        return {
            newTodoText: "test",
            todos: ["faire les courses", "promener Béné", "travailler"],
        };
    }
};
</script>

<style>

</style>