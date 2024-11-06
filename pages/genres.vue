<script setup>
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';

const API = 'http://localhost:3333/api/v1';

const route = useRoute()

const { data: genres } = await useAsyncData('genres', async () => {
  const [ genres, movies ] = await Promise.all([
    $fetch(`${API}/genres`),
    $fetch(`${API}/movies`),
  ])

  return { genres, movies }
})

const { data: moviesByGenre } = await useFetch(`${API}/movies/genre?genre_id=${route.query.genre_id}`, {
  server: false,
  lazy: false,
})
</script>

<template>
  <div class="min-h-screen text-white bg-black">
    
    <Navbar />

    <div class="flex justify-center w-full h-64 bg-black mt-15 ">
      <div class="flex justify-around  w-[1000px] pt-32">
          <a 
            v-for="genre in genres.genres"
            :href="`/genres?genre_id=${genre.id}`"
            class="flex items-center justify-center h-12 font-semibold text-black bg-white rounded-lg w-28 hover:bg-red-800 hover:text-white"
            :class="{ 'bg-red-800 text-white': activeGenre === genre.id }"
            @click="setActiveGenre(genre.id)"
          >
            {{ genre.name }}
          </a>
      </div>
    </div>

    <!-- Section Movies Start -->
    <section>
      <div class="grid grid-cols-6 gap-4 px-10 mt-15 w-[1300px] mx-auto">
        <NuxtLink 
          v-if="!route.query.genre_id"
          class="movies-card" 
          v-for="movie in genres.movies"
          :to="`/movies/${movie.id}`"
        >
          <div class="about-movies">
            <img class="movie-img" :src="movie.image" alt="poster-img" />
            <div class="movie-name"> {{ movie.title }} </div>
            <div class="detail">
              <p class="detail-duration"> {{ movie.duration }}</p>
              <p class="detail-genre"> {{ movie.genre.name }} </p>
            </div>
          </div>
        </NuxtLink>

        <NuxtLink 
          v-else
          class="movies-card" 
          v-for="movie in moviesByGenre"
          :to="`/movies/${movie.id}`"
        >
          <div class="about-movies">
            <img class="movie-img" :src="movie.image" alt="poster-img" />
            <div class="movie-name"> {{ movie.title }} </div>
            <div class="detail">
              <p class="detail-duration"> {{ movie.duration }}</p>
              <p class="detail-genre"> {{ movie.genre.name }} </p>
            </div>
          </div>
        </NuxtLink>
      </div>
    </section>
    <!-- Section Movies End -->

    <Footer />
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeGenre: null,
      genres: {
        genres: [
          { id: 1, name: 'Action' },
          { id: 2, name: 'Comedy' },
          { id: 3, name: 'Drama' },
          { id: 4, name: 'Horror' },
          { id: 5, name: 'Romance' },
          { id: 6, name: 'Thriller' },
          { id: 7, name: 'Fantasy' },
          { id: 8, name: 'Adventure' },
        ],
      },
    };
  },
  methods: {
    setActiveGenre(id) {
      this.activeGenre = id;
    },
  },
};
</script>

<style scoped>
.movies-card {
  width: 11rem;
  height: 18rem;
  margin-bottom: 4px;
  background-color: #18181b;
  border-radius: 8px; 
  cursor: pointer;
  text-align: start;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: transform 0.4s ease, background-color 0.6s, box-shadow 0.4s; 
}

.movies-card:hover {
  transform: scale(1.05); 
  background-color: black; 
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
}

.about-movies {
  color: white;
}

.movie-img {
  width: 130px;
  object-position: center;
  border-radius: 4px;
}

.movie-name {
  font-size: 18px;
  margin: 5px 0;
  color: white;
  font-weight: bolder;
  overflow: hidden;
  white-space: nowrap;
  display: inline-block;
  width: 130px;
}

.detail {
  display: flex;
  justify-content: space-between;
}

.detail-duration {
  font-weight: 400;
}

.detail-genre {
  color: #991b1b;
  font-weight: bold;
}
</style>