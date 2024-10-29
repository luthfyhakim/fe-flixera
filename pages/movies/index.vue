<script setup>
import Navbar from '../components/Navbar.vue';
import Footer from '../components/Footer.vue';

import { ref, watch } from 'vue'

const API = 'http://localhost:3333/api/v1';

const { data: movies } = await useFetch(`${API}/movies`, {
  server: false,
  lazy: false,
})

const question = ref('')
const answer = ref('Questions usually contain a question mark. ;-)')
const loading = ref(false)

watch(question, async (newQuestion, oldQuestion) => {
  if (newQuestion.includes('?')) {
    loading.value = true
    answer.value = 'Thinking...'
    try {
      const res = await useFetch(`${API}/movies`)
      answer.value = (await res.json()).answer
    } catch (error) {
      answer.value = 'Error! Could not reach the API. ' + error
    } finally {
      loading.value = false
    }
  }
})
</script>

<template>
    <div class="min-h-screen text-white bg-black">
      
        <!-- Navbar Start -->
        <Navbar />
        <!-- Navbar End -->

        <!-- Section Movies Start -->
        <section>
            <div class="search-bar">
              <input 
                type="text" 
                placeholder="Search movie here!" 
                class="search-input"
                v-model="question"
                :disabled="loading"
              />
            </div>
            <div class="grid grid-cols-6 gap-4 px-10 mt-15 w-[1300px] mx-auto">
              <NuxtLink 
                class="movies-card" 
                v-for="movie in movies" 
                :to="`/movies/${movie.id}`"
              >
                <div class="about-movies">
                    <img class="movie-img" :src="movie.image" alt="poster-img" />
                    <!-- <div :style="{ backgroundImage: `url(${movie.image})` }" class="w-[130px] h-[180px] bg-cover bg-center rounded-md"></div> -->
                    <div class="movie-name"> {{ movie.title }} </div>
                    <div class="detail">
                        <p class="detail-duration"> {{ movie.duration }}</p>
                        <p class="detail-genre"> {{ movie.genre.name }} </p>
                    </div>
                </div>
              </NuxtLink>

              <NuxtLink 
                class="movies-card" 
                v-for="movie in movies" 
                :to="`/movies/${movie.id}`"
              >
                <div class="about-movies">
                    <img class="movie-img" :src="movie.image" alt="poster-img" />
                    <!-- <div :style="{ backgroundImage: `url(${movie.image})` }" class="w-[130px] h-[180px] bg-cover bg-center rounded-md"></div> -->
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
  
      <!-- Footer Start -->
        <Footer />
      <!-- Footer End -->
    </div>
</template>

<script>
export default {
  data(){
    return {
        // searchQuery: '',
        // movies: [
        //     { id: 1, name: 'The Shadow', duration: '2h 24m', genre: 'Action', poster: '/assets/img/mov-new1.jpg'},
        //     { id: 2, name: 'Menjelang Ajal', duration: '1h 36m', genre: 'Horror', poster: '/assets/img/mov-new2.jpg'},
        //     { id: 3, name: 'Avatar 2', duration: '3h 12m', genre: 'Action', poster: '/assets/img/mov-avatar2.jpg'},
        //     { id: 4, name: 'Siksa Kubur', duration: '1h 57m', genre: 'Horror', poster: '/assets/img/mov-new4.jpg'},
        //     { id: 5, name: 'Despicable Me 4', duration: '1h 34m', genre: 'Comedy', poster: '/assets/img/mov-new5.jpeg'},
        //     { id: 6, name: 'Exhuma', duration: '2h 14m', genre: 'Horror', poster: '/assets/img/mov-exhuma.jpg'},
        // ],
    };
  },
  // computed: {
  //     filteredMovies(){
  //         return this.movies.filter(movie =>
  //             movie.name.toLowerCase().includes(this.searchQuery.toLowerCase())
  //         );
  //     },
  // },
};
</script>

<style scoped>
    .search-bar {
        padding: 50px;
        padding-top: 100px;
        display: flex;
        flex-direction: column;
        align-items: center; 
    }

    .search-input {
        width: 500px;
        border: 1px solid #991b1b;
        border-radius: 18px; 
        padding: 8px 5px;
        color: #991b1b;
        font-weight: 500; 
        outline: none;
    }

    .search-input::placeholder {
        color: #6b7280;
        padding: 10px 10px;
    }

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
