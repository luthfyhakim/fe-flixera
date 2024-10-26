<template>
    <div class="min-h-screen bg-black">
        <span class="absolute z-10 p-10 text-5xl font-bold text-white">Flixera</span>
    <div class="relative flex items-center justify-center w-full h-screen bg-black">
        <!-- Background Image and Title -->
        <div class="absolute inset-0 bg-red-900">
            <img class="object-cover w-full h-full " alt="background" src="assets/media/backsignin.png" />
        </div>
        <div class="absolute inset-0"></div>
    
        <!-- Movie Posters -->
        <div class="absolute top-[150px] w-700 flex justify-between items-center gap-3 mb-10">
            <img class="w-[210px] h-auto object-cover rounded-sm transition-transform cursor-pointer hover:scale-105 duration-100" alt="poster 1" src="assets/media/image 87.png" />
            <img class="w-[170px] h-auto object-cover rounded-sm transition-transform cursor-pointer hover:scale-105 duration-100" alt="poster 2" src="assets/media/image 84.png" />
            <img class="w-[270px] h-auto object-cover rounded-sm transition-transform cursor-pointer hover:scale-105 duration-100" alt="poster 3" src="assets/media/image 88.png" />
            <img class="w-[170px] h-auto object-cover rounded-sm transition-transform cursor-pointer hover:scale-105 duration-100" alt="poster 4" src="assets/media/image 79.png" />
            <img class="w-[210px] h-auto object-cover rounded-sm transition-transform cursor-pointer hover:scale-105 duration-100" alt="poster 5" src="assets/media/image 82.png" />
        </div>


        <div class="absolute bottom-0 w-full h-96 bg-gradient-to-t from-black"></div>
      </div>

      <div class="flex flex-col items-center justify-center w-full h-96 ">
        <div class="text-2xl text-white w-[600px] mb-14 text-center font-bold">Prices start from 54,000/month. See below for our packages and prices.</div>
        <NuxtLink to="/dashboard" class="py-4 text-xl font-bold text-white bg-red-800 shadow-2xl hover:bg-red-900 w-60 px-7 rounded-xl ">Start Subscription</NuxtLink> <!-- button -->
      </div>


      <div class="relative h-auto py-20 text-center text-white bg-black font-lato">
          <h2 class="mb-12 text-3xl font-bold">Subscription Benefits</h2>
          <!-- Benefit Cards -->
          <div class="grid max-w-6xl grid-cols-1 gap-8 px-10 mx-auto md:grid-cols-2">
            <!-- Card 1 -->
            <div class="relative p-6 rounded-lg bg-gradient-to-r from-slate-900 via-purple-900 to-slate-900 "> 
              <h3 class="mb-5 text-2xl font-semibold">Enjoy on your TV</h3>
              <p class="mb-4 text-base ">Watch on Smart TV, Playstation, Xbox, Chromecast, Apple TV, Blu-ray players, and more.</p>
            </div>
  
            <!-- Card 2 -->
            <div class="relative p-6 rounded-lg bg-gradient-to-r from-slate-900 via-purple-900 to-slate-900">
              <h3 class="mb-5 text-2xl font-semibold">Download TV shows to watch offline</h3>
              <p class="mb-4 text-base">Easily save your favorites so you always have TV shows and movies to watch.</p>
            </div>
  
            <!-- Card 3 -->
            <div class="relative p-6 rounded-lg bg-gradient-to-r from-slate-900 via-purple-900 to-slate-900">
              <h3 class="mb-5 text-2xl font-semibold">Watch anywhere</h3>
              <p class="mb-4 text-base">Stream unlimited movies and TV shows on your phone, tablet, laptop, and TV.</p>
            </div>
  
            <!-- Card 4 -->
            <div class="relative p-6 rounded-lg bg-gradient-to-r from-slate-900 via-purple-900 to-slate-900">
              <h3 class="mb-5 text-2xl font-semibold">Create a profile for your child</h3>
              <p class="mb-4 text-base">Send the kids on an adventure with their favorite characters in a world made just for them – free with your membership.</p>
            </div>
          </div>
      </div>
      
      <div id="subscription-packages" class="relative h-auto py-20 overflow-hidden text-center text-white bg-black font-lato">
        <h2 class="mb-12 text-3xl font-bold">Subscription Packages and Prices</h2>
        <p class="mb-6 text-lg text-gray-400">Choose between our Basic or Premium Plans with more streams included.</p>
        <div class="grid max-w-6xl grid-cols-1 gap-8 px-10 mx-auto md:grid-cols-2">
            <!-- Basic Plan -->
            <div class="relative p-6 rounded-lg bg-gradient-to-r from-red-900 to-black">
                <h3 class="mb-4 text-2xl font-semibold">Basic</h3>
                <p class="mb-4 text-lg">Rp 65,000/month or Rp 450,000/year</p>
                <ul class="text-left text-gray-400">
                    <li>✔ Watch all our titles</li>
                    <li>✔ On Phone/Tablet/Laptop/TV</li>
                    <li>✔ Download selected content (max 10 mobile devices)</li>
                    <li>✔ Create up to 7 profiles</li>
                    <li>✔ Max. device logins: 3 devices</li>
                    <li>✔ Concurrent streaming: 1 screen</li>
                    <li>✔ Max. video quality: Up to Full HD 1080p</li>
                </ul>
            </div>
  
            <!-- Premium Plan -->
            <div class="relative p-6 rounded-lg bg-gradient-to-r from-red-900 to-black">
                <h3 class="mb-4 text-2xl font-semibold">Premium</h3>
                <p class="mb-4 text-lg">Rp 119,000/month or Rp 799,000/year</p>
                <ul class="text-left text-gray-400">
                    <li>✔ Watch all our titles</li>
                    <li>✔ On Phone/Tablet/Laptop/TV</li>
                    <li>✔ Download selected content (max 10 mobile devices)</li>
                    <li>✔ Create up to 7 profiles</li>
                    <li>✔ Max. device logins: 10 devices</li>
                    <li>✔ Concurrent streaming: 3 screens</li>
                    <li>✔ Max. video quality: Up to 4K 2160p</li>
                </ul>
            </div>
        </div>
      </div>
    </div>
</template>
