<template>
    <li v-bind:class="{completed: todo.completed}">
        <div class="view">
            <input type="checkbox" class="toggle" v-on:change="todo.completed = !todo.completed">
            <label>{{todo.title}}</label>
            <button class="destroy" v-on:click="$emit('remove-todo', todo.id)"></button>
        </div>
        <input type="text" class="edit">
    </li>
</template>

<script>
export default {
    props: {
        todo: {
            type: Object,
            required: true
        }
    }
}
</script>
