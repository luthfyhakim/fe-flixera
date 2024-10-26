<template>
    <div class="min-h-screen text-white bg-black">
      
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
  
      <!-- Section Benner Start-->
      <section class=" relative mt-10 h-screen bg-cover bg-center bg-[url('/assets/img/backgroundmain.png')] bg-no-repeat">
            <div class="absolute inset-0 bg-gradient-to-t from-black"></div>
            <div class="absolute left-11 bottom-32">
              <h1 class="mb-4 font-bold text-8xl">Avatar 2</h1>
                <div class="flex gap-6 ">
                  <div class="px-1 py-1 font-bold border-2 border-white">PG-18</div>
                  <div>3hr 10min</div>
                  <div>2020</div>
                </div>
              <p class="w-[600px] left-[135px] text-sm mb-8 mt-2">The Way of Water is a 2022 American epic science fiction film co-produced and directed by James Cameron, who co-wrote the screenplay with Rick Jaffa</p>
              <NuxtLink to="/detailmov" class="px-6 py-3 font-semibold text-white bg-red-600 rounded-md hover:bg-red-700">Watch Now</NuxtLink>
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
            <a href="/" class="font-semibold text-red-800">View More</a>
          </div>
        </div>
  
      <div class="mx-5 mt-5">
        <div class="flex justify-evenly">
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer duration-400 hover:bg-black w-44 h-72 bg-zinc-900 hover:scale-105">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm" src="/assets/img/mov-new1.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">The Shadow</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">2h 24m</p>
                <p class="text-[15px] text-red-800 font-bold">Action</p>
              </div>
            </div>
          </div>
  
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900 ">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-new2.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">Menjelang Ajal</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">1h 36m</p>
                <p class="text-[15px] text-red-800 font-bold">Horror</p>
              </div>
            </div>
          </div>
  
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900 ">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-avatar2.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">Avatar 2</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">3h 12m</p>
                <p class="text-[15px] text-red-800 font-bold">Action</p>
              </div>
            </div>
          </div>
  
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900 ">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-new4.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">Siksa Kubur</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">1h 57 m</p>
                <p class="text-[15px] text-red-800 font-bold">Horror</p>
              </div>
            </div>
          </div>
  
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900 ">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-new5.jpeg" width="130px" />
              <div class="mb-1 text-xl font-bold">Despicable Me</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">1h 34m</p>
                <p class="text-[15px] text-red-800 font-bold">Comedy</p>
              </div>
            </div>
          </div>
  
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900 ">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-exhuma.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">Exhuma</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">2h 14m</p>
                <p class="text-[15px] text-red-800 font-bold">Horror</p>
              </div>
            </div>
          </div>
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
            <a href="/" class="font-semibold text-red-800">View More</a>
          </div>
        </div>
  
      <div class="mx-5 mt-5">
        <div class="flex justify-evenly">
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900 ">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-pop1.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">Titanic</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">3h 14m</p>
                <p class="text-[15px] text-red-800 font-bold">Romance</p>
              </div>
            </div>
          </div>
  
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900 ">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-pop2.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">Jurassic World</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">2h 4m</p>
                <p class="text-[15px] text-red-800 font-bold">Sci-fi</p>
              </div>
            </div>
          </div>
  
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900 ">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-pop3.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">Aquaman</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">2h 22m</p>
                <p class="text-[15px] text-red-800 font-bold">Adv</p>
              </div>
            </div>
          </div>
  
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900 ">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-pop4.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">Joker</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">2h 14m</p>
                <p class="text-[15px] text-red-800 font-bold">Thriller</p>
              </div>
            </div>
          </div>
  
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900 ">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-pop5.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">Parasite</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">2h 11m</p>
                <p class="text-[15px] text-red-800 font-bold">Thriller</p>
              </div>
            </div>
          </div>
  
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900 ">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-pop6.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">The Super Mari</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">1h 32m</p>
                <p class="text-[15px] text-red-800 font-bold">Comedy</p>
              </div>
            </div>
          </div>
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
            <a href="/" class="font-semibold text-red-800">View More</a>
          </div>
        </div>
  
      <div class="mx-5 mt-5">
        <div class="flex justify-evenly">
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900 ">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-rec1.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">Harlot's Prayer</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">1h 57m</p>
                <p class="text-[15px] text-red-800 font-bold">Drama</p>
              </div>
            </div>
          </div>
  
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-rec2.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">Photocopier</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">2h 10m</p>
                <p class="text-[15px] text-red-800 font-bold">Thriller</p>
              </div>
            </div>
          </div>
  
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-rec3.png" width="130px" />
              <div class="mb-1 text-xl font-bold">Purple Hearts</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">2h 2m</p>
                <p class="text-[15px] text-red-800 font-bold">Romance</p>
              </div>
            </div>
          </div>
  
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-rec4.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">Padmaavat</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">2h 44m</p>
                <p class="text-[15px] text-red-800 font-bold">Action</p>
              </div>
            </div>
          </div>
  
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-rec5.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">Cinderella</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">1h 45m</p>
                <p class="text-[15px] text-red-800 font-bold">Fantasy</p>
              </div>
            </div>
          </div>
  
          <div class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900">
            <div class="m-auto">
              <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-rec6.jpg" width="130px" />
              <div class="mb-1 text-xl font-bold">Gangubai</div>
              <div class="flex justify-between gap-1">
                <p class="text-[15px]">2h 34m</p>
                <p class="text-[15px] text-red-800 font-bold">Drama</p>
              </div>
            </div>
          </div>
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
            <a href="/" class="font-semibold text-red-800">View More</a>
          </div>
        </div>
  
        <div class="flex items-center justify-center gap-4 mt-5">
          <a href="/" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-red-600 to-yellow-200 hover:scale-105 transition-transform duration-300">Thriller</a>
          <a href="/" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-cyan-500 to-blue-500 hover:scale-105 transition-transform duration-300">Action</a>
          <a href="/" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-green-600 to-blue-500 hover:scale-105 transition-transform duration-300">Adventure</a>
          <a href="/" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-rose-500 to-fuchsia-500 hover:scale-105 transition-transform duration-300">Romance</a>
        </div>
        <div class="flex items-center justify-center gap-4 mt-5">
          <a href="/" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-blue-500 to-rose-300 hover:scale-105 transition-transform duration-300">Drama</a>
          <a href="/" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-purple-600 to-orange-500 hover:scale-105 transition-transform duration-300">Fantasy</a>
          <a href="/" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-red-500 to-black hover:scale-105 transition-transform duration-300">Horror</a>
          <a href="/" class="flex items-center justify-center w-[237px] h-[140px] text-2xl font-bold text-white rounded-xl bg-gradient-to-r from-orange-500 to-pink-500 hover:scale-105 transition-transform duration-300  ">Comedy</a>
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
            <a href="/" class="font-semibold text-red-800">View More</a>
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