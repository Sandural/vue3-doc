<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import Todo from './components/Todo.vue'

</script>

<template>
    <Todo #default="{ data }">
        <i class="fa-check-circle" :class="data.isDone ? 'fas' : 'far'"></i>
        <span class="ml-1">{{data.title}}</span>
    </Todo>
</template>

<style>
    #app {
        margin-top: 30px;
        margin-left: 30px;
    }
</style>
