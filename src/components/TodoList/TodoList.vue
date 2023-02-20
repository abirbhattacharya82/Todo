<template>
    <div class="List">
        {{ todo_list }}
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