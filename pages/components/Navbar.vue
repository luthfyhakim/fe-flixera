<template>
  <nav class="fixed top-0 left-0 z-50 w-full bg-red-800 shadow-md">
    <div class="flex items-center justify-around px-6 py-4 mx-auto ">
      <div class="text-2xl font-bold text-white">Flixera</div>
      <div class="hidden space-x-8 lg:flex">
        <NuxtLink to="/dashboard" class="text-sm font-medium">Home</NuxtLink>
        <NuxtLink to="/movies" class="text-sm font-medium">Movies</NuxtLink>
        <NuxtLink to="/genres" class="text-sm font-medium">Genres</NuxtLink>
        <NuxtLink to="/membership" class="text-sm font-medium">Membership</NuxtLink>
      </div>
    </div>
  </nav>
</template>