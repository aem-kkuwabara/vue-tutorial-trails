<script>
let id = 0

export default {
    data() {
        return {
            newTodo: '',
            todos: [
                { id: id++, text: 'Learn HTML' },
                { id: id++, text: 'Learn JavaScript' },
                { id: id++, text: 'Learn Vue' }
            ]
        }
    },
    methods: {
        addTodo() {
            this.todos.push({ id: id++, text: this.newTodo });
            this.newTodo = ''
        },
        removeTodo(target) {
            this.todos = this.todos.filter(
                function (todo) {
                    return todo !== target;
                }
            );
        }
    }
}
</script>

<template>
    <form @submit.prevent="addTodo">
        <input v-model="newTodo">
        <button>Add Todo</button>
    </form>
    <ul>
        <li v-for="todo in todos" :key="todo.id">
            {{ todo.text }}
            <button @click="removeTodo(todo)">X</button>
        </li>
    </ul>
</template>