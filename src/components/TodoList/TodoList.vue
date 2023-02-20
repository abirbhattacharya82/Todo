<template>
    <div class="List">
        <div class="Items" v-for="(item,index) in todo_list" :key="index" :id="'item-' + index">{{ item }}</div>
    </div>
</template>

<script>
export default
{
    name:'TodoList',
    props:
    {
        todo_list:Array
    }
}
</script>

<style>
.List
{
    text-align: center;
}
.List .Items
{
    font-size: 120%;
}
</style>