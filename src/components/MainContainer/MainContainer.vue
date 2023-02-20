<template>
    <div class="MainContainer">
        <Title></Title>
        <TodoList v-bind:todo_list="['item 1','item 2', 'item 3']" />
    </div>
    
</template>

<script>
import Title from '../ContainerTitle/ContainerTitle.vue';
import TodoList from '../TodoList/TodoList.vue';
export default
{
    name:'MainContainer',
    components:{
        Title,
        TodoList
    }
}
</script>

<style>
    .MainContainer
    {
        background-color: rgba(211, 211, 211, 0.514);
        width: 48%;
        padding: 1%;
    }
</style>