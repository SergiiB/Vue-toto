<template>
    <footer class="footer">
        <span class="todo-count">
            <strong></strong> items left
        </span>
        <ul class="filters">
            <li>
                <a href="#/all" class="selected">All</a>
            </li>
            <li>
                <a href="#/active" class="">Active</a>
            </li>
            <li>
                <a href="#/completed" class="">Completed</a>
            </li>
        </ul>
        <button class="clear-completed">
            Clear completed
        </button>
    </footer>
</template>

<script>
    export default {
        props: {
            index: Number
        }
    }
</script>