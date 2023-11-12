<script setup>
const todoList = [
    {text: 'Belajar html', start: '07:00', end: '08:00', done: false},
    {text: 'Belajar css', start: '08:00', end: '09:00', done: false},
    {text: 'Belajar Javascript', start: '10:00', end: '11:00', done: false},
];

const addTodo = () => {
    alert('halohalo')
}
</script>
<template>
    <div class="todolistpage">
        <h2 class="green">Todo List</h2>

        <input type="text" placeholder="Start time" v-model="startTime">
        <input type="text" placeholder="End time" v-model="endTime">
        <input type="text" placeholder="New activity" v-model="activity">
    
        <button id="btn-add" @click="addTodo">Add</button>

        <div class="todo-wrap" v-for="(item, index) in todoList">
            <button>✔️</button>
            <button>❌</button>
            {{ item.start }} - {{ item.end }} : {{ item.text }}
        </div>
    </div>
</template>
<style>
@media (min-width: 1024px) {
    .todolistpage {
        min-height: 100vh;
        display: flex;
        flex-direction: column;
        gap: 20px;
        align-items: flex-start;
        justify-content: center;
        width: max-content;
        margin: 0 auto;
    }
}
.green {
    text-align: center;
    width: 100%;
}
input {
    background: transparent;
    border: 1px solid gray;
    color: white;
    padding: 12px 10px;
    border-radius: 10px;
    width: 100%;
}

btn-add {
    width: 100%;
}

.todo-wrap {
    text-align: left;
    border-bottom: 1px solid gray;
    width: 100%;
    padding: 10px 0;
}
</style>