<template>
   <h2>ToDo Application</h2>
   <ToDoList :list="itemList" @delete="onDelete" />
   <AppendForm @append="onAppend" />
</template>

<script setup>
import AppendForm from '../components/AppendForm.vue';
import ToDoList from '../components/ToDoList.vue';
import { reactive } from 'vue';

const itemList = reactive([
   "gdhsjfksajdhgf adsg",
   "gdsahjkgfahjdsgfkjah",
   "gdsghsjdgf asgdfhjkagsdfk"
])

function onDelete(index)
{
   itemList.splice(index, 1)
}

function onAppend(newItem)
{
   itemList.push(newItem)
}

</script>