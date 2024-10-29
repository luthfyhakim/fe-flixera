<template>
  <section class="relative w-full mt-52 h-80 bg-gradient-to-t from-red-800">
    <div class="absolute w-[1000px] flex justify-between mx-auto left-0 right-0 bottom-10">
      <div class="w-[400px]">
        <div class="mb-2 text-4xl font-bold">Flixera</div>
        <p class="text-base font-sm">Flixera is the number 1 movie streaming platform and provides the best quality and is supported by a capable server, Flixera provides the best quality movie watching service and there is no charge to enjoy the movies on this site.</p>
      </div>

      <div class="w-[400px]">
        <div class="mb-2 text-2xl font-bold">Group 2</div>
        <div class="flex justify-between" v-for="name in names">
          <p>{{ name.name }}</p>
          <p>{{ name.nim }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
  export default {
    data() {
      return {
        names: [
          {
            name: "Sugeng Aldi Widodo",
            nim: "233140707111014"
          },
          {
            name: "Cagita Dian A’yunin",
            nim: "233140707111025"
          },
          {
            name: "Aulia Luthfi Hakim",
            nim: "233140707111030"
          },
          {
            name: "Nadia Alya Paramitha E.",
            nim: "233140707111031"
          },
          {
            name: "TB Rangga Gilang Yanuari",
            nim: "233140707111032"
          }
        ]
      }
    }
  }
</script>