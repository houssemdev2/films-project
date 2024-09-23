<template>
  <div class="film-list container mx-auto py-8">
    <h1 class="text-3xl font-bold text-center mb-8">Films</h1>
    <div
      class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8"
    >
      <FilmCard v-for="(film, index) in films" :key="index" :film="film" />
    </div>
  </div>
</template>

<script lang="ts" setup>
import FilmCard from "../components/FilmCard.vue";

interface Film {
  title: string;
  description: string;
  image: string;
  genres: string[];
}

// Liste des films
const films: Film[] = [
  {
    title: "Inception",
    description: "A mind-bending thriller about dreams within dreams.",
    image: "https://source.unsplash.com/400x300/?inception",
    genres: ["Sci-Fi", "Thriller", "Adventure"],
  },
  {
    title: "The Matrix",
    description: "A hacker discovers reality is a simulation.",
    image: "https://source.unsplash.com/400x300/?matrix",
    genres: ["Sci-Fi", "Action"],
  },
  {
    title: "Interstellar",
    description: "A space journey to find a new habitable planet.",
    image: "https://source.unsplash.com/400x300/?interstellar",
    genres: ["Sci-Fi", "Adventure", "Drama"],
  },
];
</script>

<style scoped>
/* Custom styles if necessary */
</style>
