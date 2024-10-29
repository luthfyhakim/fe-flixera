<script setup>
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';

const API = 'http://localhost:3333/api/v1';

const { data: movies } = await useAsyncData('genres', async () => {
  const [ genres, movies ] = await Promise.all([
    $fetch(`${API}/genres`),
    $fetch(`${API}/movies/list`)
  ])

  return { genres, movies }
})
</script>

<template>
    <div class="min-h-screen text-white bg-black">
      
      <!-- Navbar Start -->
      <Navbar />
      <!-- Navbar End -->
  
      <!-- Section Benner Start-->
      <section class="relative mt-10 h-screen bg-cover bg-center bg-[url('/assets/img/backgroundmain.png')] bg-no-repeat">
        <div class="absolute inset-0 bg-gradient-to-t from-black"></div>
        <div class="absolute left-11 bottom-32">
          <h1 class="mb-4 font-bold text-8xl">Avatar 2</h1>
            <div class="flex gap-6 ">
              <div class="px-1 py-1 font-bold border-2 border-white">PG-18</div>
              <div>3hr 10min</div>
              <div>2020</div>
            </div>
          <p class="w-[600px] left-[135px] text-sm mb-8 mt-2">The Way of Water is a 2022 American epic science fiction film co-produced and directed by James Cameron, who co-wrote the screenplay with Rick Jaffa</p>
          <NuxtLink to="/movies/1" class="px-6 py-3 font-semibold text-white bg-red-600 rounded-md hover:bg-red-700">Watch Now</NuxtLink>
        </div>
      </section>
      <!-- Section Benner End-->
  
      <!-- Section Newest Movies Start -->
      <section class="mt-24">
        <div class="flex items-center justify-center">
          <div class="flex justify-between w-[1000px] ">
            <div class="flex gap-2">
              <div class="w-2 h-5 bg-red-800"></div>
              <div class="font-bold ">Newest Movies </div>
            </div>
            <a href="/movies" class="font-semibold text-red-800">View More</a>
          </div>
        </div>
    
        <div class="mx-5 mt-5">
          <div class="flex justify-evenly">
            <NuxtLink  
              v-for="movie in movies.movies"
              class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer duration-400 hover:bg-black w-44 h-72 bg-zinc-900 hover:scale-105"
              :to="`/movies/${movie.id}`"
            >
              <div class="m-auto">
                <img class="flex items-center object-cover mb-2 rounded-sm" :src="movie.image" width="130px" />
                <div class="text-[18px] my-[5px] text-white font-extrabold overflow-hidden whitespace-nowrap inline-block w-[130px]">{{ movie.title }}</div>
                <div class="flex justify-between gap-1">
                  <p class="text-[15px]">{{ movie.duration }}</p>
                  <p class="text-[15px] text-red-800 font-bold">{{ movie.genre.name }}</p>
                </div>
              </div>
            </NuxtLink>
          </div>
        </div>
        </section>
        <!-- Section Newest Movies End -->
  
      <!-- Section Popular Movies Start -->
      <section class="mt-24">
        <div class="flex items-center justify-center">
          <div class="flex justify-between w-[1000px] ">
            <div class="flex gap-2">
              <div class="w-2 h-5 bg-red-800"></div>
              <div class="font-bold ">Popular Movies</div>
            </div>
            <a href="/movies" class="font-semibold text-red-800">View More</a>
          </div>
        </div>
  
      <div class="mx-5 mt-5">
        <div class="flex justify-evenly">
          <NuxtLink 
            v-for="movie in movies.movies"
            class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900"
            :to="`/movies/${movie.id}`"
          >
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " :src="movie.image" width="130px" />
              <div class="text-[18px] my-[5px] text-white font-extrabold overflow-hidden whitespace-nowrap inline-block w-[130px]">{{ movie.title }}</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">{{ movie.duration }}</p>
                <p class="text-[15px] text-red-800 font-bold">{{ movie.genre.name }}</p>
              </div>
            </div>
          </NuxtLink>
        </div>
      </div>
      </section>
      <!-- Section Popular Movies Start -->
  
      <!-- Section Recommendation Start -->
      <section class="mt-24">
        <div class="flex items-center justify-center">
          <div class="flex justify-between w-[1000px] ">
            <div class="flex gap-2">
              <div class="w-2 h-5 bg-red-800"></div>
              <div class="font-bold ">Recommendation Movies</div>
            </div>
            <a href="/movies" class="font-semibold text-red-800">View More</a>
          </div>
        </div>
  
      <div class="mx-5 mt-5">
        <div class="flex justify-evenly">
          <NuxtLink 
            v-for="movie in movies.movies"
            class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900"
            :to="`/movies/${movie.id}`"
          >
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " :src="movie.image" width="130px" />
              <div class="text-[18px] my-[5px] text-white font-extrabold overflow-hidden whitespace-nowrap inline-block w-[130px]">{{ movie.title }}</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">{{ movie.duration }}</p>
                <p class="text-[15px] text-red-800 font-bold">{{ movie.genre.name }}</p>
              </div>
            </div>
          </NuxtLink>
        </div>
      </div>
      </section>
      <!-- Section Recommendation Start -->
  
      <!-- Genre Movies Start -->
      <section class="mt-24">
        <div class="flex items-center justify-center">
          <div class="flex justify-between w-[1000px] ">
            <div class="flex gap-2">
              <div class="w-2 h-5 bg-red-800"></div>
              <div class="font-bold ">Genres </div>
            </div>
            <a href="/genres" class="font-semibold text-red-800">View More</a>
          </div>
        </div>
  
        <div class="flex items-center justify-center gap-4 mt-5">
          <a :href="`/genres?genre_id=${movies.genres[0].id}`" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-red-600 to-yellow-200 hover:scale-105 transition-transform duration-300">{{ movies.genres[0].name }}</a>
          <a :href="`/genres?genre_id=${movies.genres[1].id}`" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-cyan-500 to-blue-500 hover:scale-105 transition-transform duration-300">{{ movies.genres[1].name }}</a>
          <a :href="`/genres?genre_id=${movies.genres[2].id}`" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-green-600 to-blue-500 hover:scale-105 transition-transform duration-300">{{ movies.genres[2].name }}</a>
          <a :href="`/genres?genre_id=${movies.genres[3].id}`" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-rose-500 to-fuchsia-500 hover:scale-105 transition-transform duration-300">{{ movies.genres[3].name }}</a>
        </div>
        <div class="flex items-center justify-center gap-4 mt-5">
          <a :href="`/genres?genre_id=${movies.genres[4].id}`" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-blue-500 to-rose-300 hover:scale-105 transition-transform duration-300">{{ movies.genres[4].name }}</a>
          <a :href="`/genres?genre_id=${movies.genres[5].id}`" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-purple-600 to-orange-500 hover:scale-105 transition-transform duration-300">{{ movies.genres[5].name }}</a>
          <a :href="`/genres?genre_id=${movies.genres[6].id}`" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-red-500 to-black hover:scale-105 transition-transform duration-300">{{ movies.genres[6].name }}</a>
          <a :href="`/genres?genre_id=${movies.genres[7].id}`" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-orange-500 to-pink-500 hover:scale-105 transition-transform duration-300  ">{{ movies.genres[7].name }}</a>
        </div>
      </section>
      <!-- Genre Movies Start -->
  
      <!-- Upcoming Movies Start -->
       <section class="mt-24">
        <div class="flex items-center justify-center">
          <div class="flex justify-between w-[1000px] ">
            <div class="flex gap-2">
              <div class="w-2 h-5 bg-red-800"></div>
              <div class="font-bold ">Upcoming Movies</div>
            </div>
            <a href="/movies" class="font-semibold text-red-800">View More</a>
          </div>
        </div>
  
        <div class="flex items-center justify-center">
          <div class="flex justify-between w-[1000px] mt-6">
            <img src="/assets/img/2690334.jpg" alt="" width="485px" class="rounded-xl">
            <img src="/assets/img/2690334.jpg" alt="" width="485px" class="rounded-xl">
          </div>        
        </div>
  
       </section>
      <!-- Upcoming Movies End -->
      
  
      <!-- Footer Start -->
      <Footer />
      <!-- Footer End -->
    </div>
  </template>