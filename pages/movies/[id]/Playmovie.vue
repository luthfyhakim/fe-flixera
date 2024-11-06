<script setup>
import Navbar from '../../components/Navbar.vue';
import Footer from '../../components/Footer.vue';

const API = 'http://localhost:3333/api/v1';

const route = useRoute()

const { data: movies } = await useAsyncData('genres', async () => {
  const [ genres, moviesById ] = await Promise.all([
    $fetch(`${API}/genres`),
    $fetch(`${API}/movies/${route.params.id}`)
  ])

  return { genres, moviesById }
})
</script>

<template>
  <div class="min-h-screen text-white bg-black">
    <div class="relative w-full min-h-screen overflow-y-auto text-left text-white bg-black font-lato">  
      
      <!-- Navbar Start -->
      <Navbar />
      <!-- Navbar End -->
    
      <!-- Background Image Section -->
      <div class="mt-[60px] w-full max-w-[1440px] mx-auto h-[766px] relative">
        <iframe class="w-full h-full object-cove" width="560" height="315" :src="movies.moviesById.video" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
      </div>

        
        <!-- Movie Details Section -->
        <div class="w-full max-w-[1171px] mx-auto px-6 py-12 text-2xl">
          <div class="relative w-full h-auto">
            <h1 class="font-bold tracking-tight text-white text-7xl drop-shadow-lg">{{ movies.moviesById.title }}</h1>
            <div class="flex mt-6 space-x-6">
              <span class="px-2 py-1 text-xl font-semibold border border-white">18+</span>
              <span class="text-xl font-semibold">{{ movies.moviesById.duration }}</span>
              <span class="text-xl font-semibold">{{ movies.moviesById.releaseYear }}</span>
              <span class="text-xl font-semibold">{{ movies.moviesById.genre.name }}</span>
            </div>
            <p class="mt-4 text-lg text-justify text-gray-400">
              {{ movies.moviesById.description }}
            </p>
          </div>
        </div>
    
        <!-- Trailer & Extra Section -->
        <div class="w-full max-w-[1171px] mx-auto px-6 py-12">
          <h2 class="mb-4 text-3xl font-medium capitalize">Trailer & Ekstra</h2>
          <div class="flex gap-4">
            <img class="object-cover w-full h-auto max-w-md rounded-md " alt="Trailer Thumbnail" :src="movies.moviesById.trailerimg1" />
            <img class="object-cover w-full h-auto max-w-md rounded-md " alt="Trailer Thumbnail" :src="movies.moviesById.trailerimg2" />
          </div>
        </div>
    
        <!-- Recommendations Section -->
        <div class="w-full max-w-[1165px] mx-auto px-6 py-12 text-center">
            <h2 class="my-16 text-2xl font-bold capitalize">Recommendations for you</h2>
            <div class="grid grid-cols-5 gap-8">
              <img class="object-cover w-full h-auto rounded-md" alt="Mencuri Raden Saleh" src="assets/media/image 79.png" />
              <img class="object-cover w-full h-auto rounded-md" alt="Trap" src="assets/media/image 80.png" />
              <img class="object-cover w-full h-auto rounded-md" alt="13 Bom Jakarta" src="assets/media/image 81.png " />
              <img class="object-cover w-full h-auto rounded-md" alt="Movie Poster 4" src="assets/media/image 88.png" />
              <img class="object-cover w-full h-auto rounded-md" alt="Movie Poster 5" src="assets/media/image 83.png" />
              <img class="object-cover w-full h-auto rounded-md" alt="Movie Poster 6" src="assets/media/image 84.png" />
              <img class="object-cover w-full h-auto rounded-md" alt="Movie Poster 7" src="assets/media/image 85.png" />
              <img class="object-cover w-full h-auto rounded-md" alt="Movie Poster 8" src="assets/media/image 86.png" />
              <img class="object-cover w-full h-auto rounded-md" alt="Movie Poster 9" src="assets/media/image 87.png" />
              <img class="object-cover w-full h-auto rounded-md" alt="Movie Poster 9" src="assets/media/dilan1990.jpg" />
            </div>
          </div>  
        </div>

      <!-- Footer Start -->
      <Footer />
      <!-- Footer End -->
  </div>
</template>