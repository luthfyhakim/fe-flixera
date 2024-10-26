<template>
    <div class="min-h-screen text-white bg-black">
      
      <!-- Navbar Start -->
      <nav class="fixed top-0 left-0 z-50 w-full bg-red-800 shadow-md">
        <div class="flex items-center justify-around px-6 py-4 mx-auto ">
          <div class="text-2xl font-bold text-white">Flixera</div>
          <div class="hidden space-x-8 lg:flex">
            <NuxtLink to="/dashboard" class="text-sm font-medium">Home</NuxtLink>
            <NuxtLink to="/allmov" class="text-sm font-medium">Movies</NuxtLink>
            <NuxtLink to="#" class="text-sm font-medium">Genres</NuxtLink>
            <NuxtLink to="/membership" class="text-sm font-medium">Membership</NuxtLink>
          </div>
        </div>
      </nav>
      <!-- Navbar End -->

      <div class="flex justify-center w-full h-64 bg-black mt-15 ">
        <div class="flex justify-around  w-[1000px] pt-32  ">
            <a href="#" class="flex items-center justify-center h-12 font-semibold text-black bg-white rounded-lg w-28 hover:bg-red-800 hover:text-white ">Thriller</a>
            <a href="#" class="flex items-center justify-center h-12 font-semibold text-black bg-white rounded-lg w-28 hover:bg-red-800 hover:text-white ">Action</a>
            <a href="#" class="flex items-center justify-center h-12 font-semibold text-black bg-white rounded-lg w-28 hover:bg-red-800 hover:text-white ">Adventure</a>
            <a href="#" class="flex items-center justify-center h-12 font-semibold text-black bg-white rounded-lg w-28 hover:bg-red-800 hover:text-white ">Romance</a>
            <a href="#" class="flex items-center justify-center h-12 font-semibold text-black bg-white rounded-lg w-28 hover:bg-red-800 hover:text-white ">Drama</a>
            <a href="#" class="flex items-center justify-center h-12 font-semibold text-black bg-white rounded-lg w-28 hover:bg-red-800 hover:text-white ">Fantasy</a>
            <a href="#" class="flex items-center justify-center h-12 font-semibold text-black bg-white rounded-lg w-28 hover:bg-red-800 hover:text-white ">Horror</a>
            <a href="#" class="flex items-center justify-center h-12 font-semibold text-black bg-white rounded-lg w-28 hover:bg-red-800 hover:text-white ">Comedy</a>
        </div>
      </div>
  
      <!-- Section Movies Start -->
    <section class="">
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
            <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-new3.jpg" width="130px" />
            <div class="mb-1 text-xl font-bold">Fighter</div>
            <div class="flex justify-between gap-1">
              <p class="text-[15px]">2h 46m</p>
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

        <NuxtLink to="/detailmov" class="flex flex-col items-center p-3 text-white transition-transform rounded-md cursor-pointer hover:scale-105 duration-400 hover:bg-black w-44 h-72 bg-zinc-900 ">
          <div class="m-auto">
            <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-avatar2.jpg" width="130px" />
            <div class="mb-1 text-xl font-bold">Avatar 2</div>
            <div class="flex justify-between gap-1">
              <p class="text-[15px]">3h 12m</p>
              <p class="text-[15px] text-red-800 font-bold">Action</p>
            </div>
          </div>
        </NuxtLink>

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
            <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-new3.jpg" width="130px" />
            <div class="mb-1 text-xl font-bold">Fighter</div>
            <div class="flex justify-between gap-1">
              <p class="text-[15px]">2h 46m</p>
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
            <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-new3.jpg" width="130px" />
            <div class="mb-1 text-xl font-bold">Fighter</div>
            <div class="flex justify-between gap-1">
              <p class="text-[15px]">2h 46m</p>
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
            <img class="flex items-center object-cover mb-2 rounded-sm " src="/assets/img/mov-new3.jpg" width="130px" />
            <div class="mb-1 text-xl font-bold">Fighter</div>
            <div class="flex justify-between gap-1">
              <p class="text-[15px]">2h 46m</p>
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
    <!-- Section Movies End -->
  
      <!-- Footer Start -->
      <section class="relative w-full mt-96 h-80 bg-gradient-to-t from-red-800">
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