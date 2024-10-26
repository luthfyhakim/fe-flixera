<template>
  <span class="absolute z-10 p-12 text-5xl font-bold text-white">Flixera</span>
  <div class="absolute z-20 flex space-x-4 top-10 right-10">
    <select class="px-4 py-2 text-white bg-black border border-gray-600 rounded cursor-pointer bg-opacity-70 border-gray">
      <option>Bahasa Indonesia</option>
      <option>English</option>
    </select>
    <button class="px-4 py-2 font-bold text-white transition bg-red-600 rounded-md hover:bg-red-700">
      <NuxtLink to="/login">Sign In</NuxtLink>
    </button>
  </div>
  
  <div class="flex flex-col items-center justify-center min-h-screen text-white bg-red-900">
    <p class="w-[950px] text-l mb-6 text-center tracking-wide">Ready to watch? Click this button to create or restart your membership.</p>
    <h1 class="w-[950px] text-5xl font-bold mb-6 text-center tracking-wide">Create your account to enjoy the latest movies</h1>
    <div class="w-full max-w-md p-8 bg-opacity-75 rounded-md">
      <form @submit.prevent="register">
        <div class="flex items-center mb-4 space-x-4">
          <input
            v-model="email"
            id="email"
            type="email"
            required
            class="w-full p-3 mt-2 bg-black border border-gray-600 rounded-md bg-opacity-70"
            placeholder="Enter your email address"
          />            
          <NuxtLink to="/login" type="submit" class="p-3 font-bold text-white transition bg-red-600 rounded-md w-60 hover:bg-red-700">
            Get Started
          </NuxtLink> <!-- button -->
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: '',
    }
  },
  methods: {
    register() {
      console.log('Email:', this.email)
      // Handle the registration logic here, e.g., send it to a server.
    },
  },
}
</script>

<style scoped>
.bg-red-900 {
  background-image: url('assets/media/backsignin.png');
  background-size: cover;
  background-position: center;
}
</style>
