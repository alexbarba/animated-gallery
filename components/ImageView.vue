<template>
  <div class="h-full transition-all duration-150 flex-1 m-2 relative flex">
    <img class="object-fill w-full rounded" :src="src" alt="img" />

    <div
      class="absolute top-0 content-center flex-wrap justify-center text-white bg-gray-500 bg-opacity-50 min-h-full min-w-full z-50 opacity-0 hover:opacity-100 divide-y-2 divide-white divide-opacity-100"
    >
      <div class="p-2">
        <h1 class="text-center text-xl font-bold">{{ title }}</h1>
      </div>

      <div class="p-2">
        <p class="text-center">{{ description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ImageView',
  props: {
    src: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
  },
}
</script>

<style></style>
