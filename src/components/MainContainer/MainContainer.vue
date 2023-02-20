<template>
    <div class="MainContainer">
        <Title></Title>
        <TodoList v-bind:todo_list=todo />
        <div class="Button_area">
            <button @click="clearAll()">Clear All</button>
        </div>
        <div class="NewTodo">
            <input type="text" id="new_task"> <button @click="addtask()">Add</button>
        </div>
        <InstructionList />
    </div>
    
</template>

<script>
import Title from '../ContainerTitle/ContainerTitle.vue';
import TodoList from '../TodoList/TodoList.vue';
import InstructionList from '../InstructionList/InstructionList.vue';
export default
{
    name:'MainContainer',
    components:{
        Title,
        TodoList,
        InstructionList
    },
    data(){
        return{
            todo:[]
        }
    },
    methods:{
        addtask()
        {
            var new_task=document.getElementById('new_task').value;
            this.todo.push(''+new_task);
            document.getElementById('new_task').value="";
        },
        clearAll()
        {
            this.todo=[];
        }
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
    .Button_area
    {
        width: 100%;
        text-align: center;
        margin-top: 1%;
    }
    .Button_area button
    {
        background-color: rgb(255, 61, 61);
        border: none;
        color: white;
        padding: 1%;
    }
    .Button_area button:hover
    {
        background-color: rgb(124, 0, 0);
    }
    .NewTodo
    {
        width: 100%;
        display: flex;
        justify-content: center;
        margin-top: 1%;
    }
    .NewTodo input
    {
        outline: none;
        border: none;
        border-bottom: 1px solid black;
        background-color: transparent;
        margin-right: 1%;
        width: 70%;
    }
    .NewTodo button
    {
        background-color: rgb(74, 61, 255);
        border: none;
        color: white;
        padding: 1%;
    }
    .NewTodo button:hover
    {
        background-color: rgb(0, 23, 124);
    }
</style>