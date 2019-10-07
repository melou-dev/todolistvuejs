<template>
    <div>
        <TodoInputText v-model="newTodoText" @keydown.enter="addTodo" />
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
    },
    methods: {
        addTodo() {
            const textTrimmed = this.newTodoText.trim();
            if(textTrimmed) {
                this.todos.push(textTrimmed);
                textTrimmed = "";
            }
        }
    }
};
</script>

<style>

</style>