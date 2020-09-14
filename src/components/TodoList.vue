<template>
    <section class="main">
        <input id="toggle-all" type="checkbox" class="toggle-all">
        <label for="toggle-all">Mark all as complete</label>
        <ul class="todo-list">
            <TodoItem v-for="(todo, i) in todos"
                      v-bind:todo="todo"
                      v-bind:index="i"
                      v-on:remove-todo="removeTodo"

            />
        </ul>
    </section>
</template>

<script>
import TodoItem from './TodoItem'

export default {
    components: {TodoItem},
    props: ['todos'],
    comments: {
        TodoItem
    },
    methods: {
        removeTodo(id) {
            this.$emit('remove-todo', id)
        }
    }
}
</script>