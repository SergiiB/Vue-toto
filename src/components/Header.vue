<template>
    <header class="header">
        <h1>todos</h1>
        <form v-on:submit.prevent.keyup.enter="onSubmit">
            <input v-model="title"
                   autofocus="autofocus"
                   autocomplete="off"
                   placeholder="What needs to be done?"
                   class="new-todo">
        </form>
    </header>
</template>

<script>
    export default {
        data() {
            return {
                title: ''
            }
        },
        methods: {
            onSubmit() {
                if(this.title.trim()) {
                    const newTodoItem = {
                        id: Date.now(),
                        title: this.title,
                        completed: false
                    };

                    this.$emit('add-todo-item', newTodoItem);
                    this.title = ''
                }
            }
        }
    }
</script>