<template>
   <div>
      <div class="item-content">{{ content }}
         <span class="item-button" @click="onClick"> [X]</span>
      </div>
   </div>
</template>

<script setup>
defineProps(['content'])
const emit = defineEmits(['mydelete'])

function onClick()
{
   emit('mydelete');
}

</script>

<style>
.item-content {
   margin: 15px;
}

.item-button {}
</style>