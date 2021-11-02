<template>
    <ul>
        <li v-for="item in todos" :key="item.id"
            @click="changeItemStatus(item.id)"
            class="p-1 mb-1 px-2 cursor-pointer"
            :class="item.isDone ? 'bg-red-100' : ''">
            <slot :data="item"></slot>
        </li>
    </ul>
</template>

<script setup>
import {reactive} from 'vue'

const todos = reactive([
    {id: 1, title: '办理业务', isDone: false},
    {id: 2, title: '完成家庭作业', isDone: true},
    {id: 3, title: '上计算机课', isDone: false},
])

const changeItemStatus = (id) => {
    todos.filter(v => v.id === id).map(j => j.isDone = !j.isDone)
}
</script>

<style scoped>

</style>
