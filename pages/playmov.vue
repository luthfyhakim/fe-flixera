<template>
  <div class="min-h-screen text-white bg-black">
    <div class="relative w-full min-h-screen overflow-y-auto text-left text-white bg-black font-lato">  
      
      <!-- Navbar Start -->
      <nav class="fixed top-0 left-0 z-50 w-full bg-red-800 shadow-md">
        <div class="flex items-center justify-around px-6 py-4 mx-auto ">
          <div class="text-2xl font-bold text-white">Flixera</div>
          <div class="hidden space-x-8 lg:flex">
            <NuxtLink to="#" class="text-sm font-medium">Home</NuxtLink>
            <NuxtLink to="/allmov" class="text-sm font-medium">Movies</NuxtLink>
            <NuxtLink to="/genres" class="text-sm font-medium">Genres</NuxtLink>
            <NuxtLink to="/membership" class="text-sm font-medium">Membership</NuxtLink>
          </div>
        </div>
      </nav>
      <!-- Navbar End -->
    
      <!-- Background Image Section -->
      <div class="mt-[60px] w-full max-w-[1440px] mx-auto h-[766px] relative">
      <iframe class="w-full h-full object-cove" width="560" height="315" src="https://www.youtube.com/embed/d9MyW72ELq0?si=qQ5vPFbQNTGNlDHh" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
      </div>

        
        <!-- Movie Details Section -->
        <div class="w-full max-w-[1171px] mx-auto px-6 py-12 text-2xl">
          <div class="relative w-full h-auto">
            <h1 class="font-bold tracking-tight text-white text-7xl drop-shadow-lg">Avatar 2</h1>
            <div class="flex mt-6 space-x-6">
              <span class="px-2 py-1 text-xl font-semibold border border-white">18+</span>
              <span class="text-xl font-semibold">3hr 10min</span>
              <span class="text-xl font-semibold">2020</span>
              <span class="text-xl font-semibold">Action</span>
            </div>
            <p class="mt-4 text-lg text-justify text-gray-400">
              The sequel to the film "Avatar", directed by James Cameron, once again focuses on Jake Sully (played by Sam Worthington), who has now become part of the Na'vi tribe on Pandora. Jake and Neytiri (Zoe Saldana) are living peacefully with their children, but their peace is disrupted when humans return to Pandora with the intention of exploiting its valuable resources. The film introduces a new region of Pandora, the beautiful oceans teeming with spectacular marine life. Jake's family must collaborate with the sea-dwelling Metkayina clan, led by Tonowari (Cliff Curtis), to face a new threat from humans seeking to exploit their planet. Additionally, a personal threat from Jake's past reappears in the form of Colonel Miles Quaritch (Stephen Lang), who has now returned as a Na'vi avatar.
            </p>
          </div>
        </div>
    
        <!-- Trailer & Extra Section -->
        <div class="w-full max-w-[1171px] mx-auto px-6 py-12">
          <h2 class="mb-4 text-3xl font-medium capitalize">Trailer & Ekstra</h2>
          <div class="flex gap-4">
            <img class="object-cover w-full h-auto max-w-md rounded-md " alt="Trailer Thumbnail" src="/assets/media/trailerimg1.png" />
            <img class="object-cover w-full h-auto max-w-md rounded-md " alt="Trailer Thumbnail" src="/assets/media/trailerimg2.jpg" />
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
      <section class="relative w-full mt-52 h-80 bg-gradient-to-t from-red-800">
        <div class="absolute w-[1000px] flex justify-between mx-auto left-0 right-0 bottom-10">
          <div class="w-[400px]">
            <div class="mb-2 text-4xl font-bold">Flixera</div>
            <p class="text-base font-sm">Flixera is the number 1 movie streaming platform and provides the best quality and is supported by a capable server, Flixera provides the best quality movie watching service and there is no charge to enjoy the movies on this site.</p>
          </div>
  
          <div class="w-[400px]">
            <div class="mb-2 text-2xl font-bold">Group 2</div>
            <div class="flex justify-between">
              <p>Sugeng Aldi Widodo</p>
              <p>233140707111014</p>
            </div>
            <div class="flex justify-between">
              <p>Cagita Dian A’yunin</p>
              <p>233140707111025</p>
            </div>
            <div class="flex justify-between">
              <p>Aulia Luthfi Hakim</p>
              <p>233140707111030</p>
            </div>
            <div class="flex justify-between">
              <p>Nadia Alya Paramitha E.</p>
              <p>233140707111031</p>
            </div>
            <div class="flex justify-between">
              <p>TB Rangga Gilang Yanuari </p>
              <p>233140707111032</p>
            </div>
          </div>
        </div>
      </section>
      <!-- Footer End -->
  </div>
</template>