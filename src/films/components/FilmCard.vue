<template>
  <div class="max-w-sm rounded overflow-hidden shadow-lg bg-white">
    <img class="w-full" :src="film.image" alt="Movie poster" />
    <div class="px-6 py-4">
      <div class="font-bold text-xl mb-2">{{ film.title }}</div>
      <p class="text-gray-700 text-base">
        {{ film.description }}
      </p>
    </div>
    <div class="px-6 pt-4 pb-2">
      <span
        v-for="genre in film.genres"
        :key="genre"
        class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2"
      >
        #{{ genre }}
      </span>
    </div>
  </div>
</template>

<script lang="ts" setup>
interface Film {
  title: string;
  description: string;
  image: string;
  genres: string[];
}

// Props
const props = defineProps<{ film: Film }>();
</script>

<style scoped>
/* Custom styles, if necessary */
</style>
