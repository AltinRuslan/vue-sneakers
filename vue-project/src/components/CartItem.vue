<script setup>
const emit = defineEmits(['onClickRemove'])


  defineProps({
    id: Number,
    title: String,
    imageUrl: String,
    price: Number
  })
</script>

<template>
  <div class="flex border items-center border-slate-100 p-4 rounded-xl gap-4">
    <img class="w-16 h-16" :src="imageUrl" :alt="title">
    <div class="flex flex-col flex-1 ">
      <p>{{ title}}</p>

      <div class="flex justify-between mt-2">
        <b class="flex-1">{{  price }}</b>
        <img @click="emit('onClickRemove')" src="/close.svg" class="opacity-40 hover:opacity-100 cursor-pointer transition"/>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>
