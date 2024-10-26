<template>
  <span class="absolute z-10 text-5xl font-bold text-white p-14">Flixera</span>
  <div class="relative flex items-center justify-center w-full h-screen bg-black">
    <!-- Background Image -->
    <div class="absolute inset-0 bg-red-900">
      <img class="object-cover w-full h-full opacity-95" src="assets/media/backsignin.png" alt="Background Image"/>
    </div>
    <div class="absolute inset-0"></div>

    <!-- Login Card -->
    <div class="relative z-10 px-8 py-10 bg-black rounded-lg shadow-lg bg-opacity-60">
      <h2 class="px-4 mb-10 text-3xl font-semibold text-white">Sign In</h2>

      <form @submit.prevent="handleSubmit">
        <!-- Email Input -->
        <div class="flex justify-center mb-6">
          <input
            id="email"
            type="text"
            class="px-3 py-2 text-white bg-black border border-gray-600 rounded w-72 bg-opacity-80"
            placeholder="Email or phone number"
            v-model="email"
          />
        </div>

        <!-- Password Input -->
        <div class="flex justify-center mb-6">
          <input
            id="password"
            type="password"
            class="px-3 py-2 text-white bg-black border border-gray-600 rounded w-72 bg-opacity-80"
            placeholder="Password"
            v-model="password"
          />
        </div>

        <!-- Sign In Button -->
        <div class="flex justify-center mb-6">
          <NuxtLink to="/membership" type="submit" class="px-3 py-2 font-semibold text-center text-white bg-red-600 rounded w-72 hover:bg-red-800">Sign In</NuxtLink> <!-- button -->
        </div>

        <!-- Forgot Password -->
        <div class="mb-4 text-center">
          <a href="#" class="text-gray-400 hover:text-white">Forgot Password?</a>
        </div>

        <!-- Remember Me & Need Help -->
        <div class="flex items-center justify-between mb-6 text-white">
          <label>
            <input type="checkbox" class="mr-2" />
            Remember me
          </label>
          <a href="#" class="text-gray-400 hover:text-white">Need Help?</a>
        </div>

        <!-- Register Now -->
        <div class="text-center text-gray-400">
          New to Flixera?``
          <NuxtLink class="text-yellow-400 hover:text-yellow-500" to="/register">Sign Up Now</NuxtLink> <!--- button -->
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      email: '',
      password: '',
    };
  },
  methods: {
    handleSubmit() {
      // Implement logic to handle form submission
      console.log('Email:', this.email);
      console.log('Password:', this.password);
    },
  },
};
</script>

<style scoped>
/* You can add custom styles here if needed */
</style>
