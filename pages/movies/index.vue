<script setup>
import Navbar from '../components/Navbar.vue';
import Footer from '../components/Footer.vue';

const API = 'http://localhost:3333/api/v1';

const { data: movies } = await useFetch(`${API}/movies`, {
  server: false,
  lazy: false,
})
</script>

<template>
    <div class="min-h-screen text-white bg-black">
      
        <Navbar />

        <!-- Section Movies Start -->
        <section>
            <div class="search-bar">
              <input 
                type="text" 
                placeholder="Search movie here!" 
                class="search-input"
                v-model="searchQuery"
              />
            </div>
            
            
            <div class="grid grid-cols-6 gap-4 px-10 mt-15 w-[1300px] mx-auto">
              <div v-if="isLoading">Loading...</div>
              
              <NuxtLink 
                v-if="results.length"
                class="movies-card" 
                v-for="(movie, index) in results" 
                :key="index"
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

              <div v-if="!isLoading && !results.length && searchQuery">No Results Found</div>

              <NuxtLink 
                v-if="!searchQuery"
                class="movies-card" 
                v-for="movie in movies" 
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
  
      <!-- Footer Start -->
        <Footer />
      <!-- Footer End -->
    </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      searchQuery: '',
      results: [],
      isLoading: false,
      debounceTimeout: null,
    }
  },

  watch: {
    searchQuery(newQuery) {
      clearTimeout(this.debounceTimeout);

      if (newQuery) {
        this.debounceTimeout = setTimeout(() => {
          this.fetchResults(newQuery);
        }, 300)
      } else {
        this.results = [];
      }
    }
  },

  methods: {
    async fetchResults(query) {
      this.isLoading = true;

      try {
        const response = await axios.get(`http://localhost:3333/api/v1/movies?title=${query}`);
        this.results = response.data;
      } catch (error) {
        console.error('Error fetching data:', error);
        this.results = [];
      } finally {
        this.isLoading = false;
      }
    }
  }
}
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
