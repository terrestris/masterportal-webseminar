<script>
export default {
  props: {
    title: {
      type: String,
    },
  }
}
</script>

<template>
  <div v-if="title || social" class="flex flex-row bg-barBottom absolute w-full bottom-0 left-0 text-lg">
      <div class="basis-5" />
      <div class="basis-8" />
      <div class="basis-auto">4</div>
  </div>
</template>
