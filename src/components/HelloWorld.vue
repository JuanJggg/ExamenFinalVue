<script setup>

const props= defineProps({
  user:{}
})

console.log(props)
</script>

<template>
  <h1 class="text-4xl ml-8 mt-8 font-semibold text-white">{{ props.user.name  }}</h1>
  <div class="bg-slate-700 mx-8 rounded-lg h-[90px] mt-8">
    <p class="text-xl ml-4 pt-7 text-white">{{ props.user.mensaje1 }}</p>
  </div>
  <div class="bg-slate-700 mx-8 rounded-lg h-[90px] mt-8">
    <p class="text-xl ml-4 pt-7 text-white">{{ props.user.mensaje2 }}</p>
  </div>
  <div class="bg-slate-700 mx-8 rounded-lg h-[90px] mt-8">
    <p class="text-xl ml-4 pt-7 text-white">{{ props.user.mensaje3 }}</p>
  </div>
</template>

