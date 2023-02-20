<template>
    <div class="List">
        {{ todo_list[0] }}
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