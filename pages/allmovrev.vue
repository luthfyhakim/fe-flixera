<template>
    <div class="min-h-screen text-white bg-black">
      
        <!-- Navbar Start -->
        <nav class="fixed top-0 left-0 z-10 w-full bg-red-800 shadow-md">
            <div class="flex items-center justify-around px-6 py-4 mx-auto ">
            <div class="text-2xl font-bold text-white">Flixera</div>
            <div class="hidden space-x-8 lg:flex">
                <NuxtLink to="/dashboard" class="text-sm font-medium">Home</NuxtLink>
                <NuxtLink to="#" class="text-sm font-medium">Movies</NuxtLink>
                <NuxtLink to="/genres" class="text-sm font-medium">Genres</NuxtLink>
                <NuxtLink to="/membership" class="text-sm font-medium">Membership</NuxtLink>
            </div>
            </div>
        </nav>
        <!-- Navbar End -->

        <!-- Section Movies Start -->
        <section>
        <div class="search-bar">
            <input 
            type="text" 
            placeholder="search movie here!" 
            class="search-input"
            v-model="searchQuery">
        </div>
        <div class="grid grid-cols-6 gap-4 px-10 mt-28">
            <div class="movies-card" v-for="movie in filteredMovies" :key="movie.id">
                <div class="about-movies">
                    <!-- <img :src="movie.poster" alt="poster-img" class="movie-img"> -->
                    <div :style="{ backgroundImage: `url(${movie.poster})` }" class="w-[130px] h-[180px] bg-cover bg-center rounded-md"></div>
                    <div class="movie-name"> {{ movie.name }} </div>
                    <div class="detail">
                        <p class="detail-duration"> {{ movie.duration }} </p>
                        <p class="detail-genre"> {{ movie.genre }} </p>
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

<script>
export default {
    data(){
        return {
            searchQuery: '',
            movies: [
                { id: 1, name: 'The Shadow', duration: '2h 24m', genre: 'Action', poster: '/assets/img/mov-new1.jpg'},
                { id: 2, name: 'Menjelang Ajal', duration: '1h 36m', genre: 'Horror', poster: '/assets/img/mov-new2.jpg'},
                { id: 3, name: 'Avatar 2', duration: '3h 12m', genre: 'Action', poster: '/assets/img/mov-avatar2.jpg'},
                { id: 4, name: 'Siksa Kubur', duration: '1h 57m', genre: 'Horror', poster: '/assets/img/mov-new4.jpg'},
                { id: 5, name: 'Despicable Me 4', duration: '1h 34m', genre: 'Comedy', poster: '/assets/img/mov-new5.jpeg'},
                { id: 6, name: 'Exhuma', duration: '2h 14m', genre: 'Horror', poster: '/assets/img/mov-exhuma.jpg'},
            ],
        };
    },
    computed: {
        filteredMovies(){
            return this.movies.filter(movie =>
                movie.name.toLowerCase().includes(this.searchQuery.toLowerCase())
            );
        },
    },
};
</script>

<style scoped>
    .search-bar {
        padding: 50px;
        padding-top: 100px;
        display: flex;
        flex-direction: column;
        align-items: center; 
    }

    .search-input {
        width: 500px;
        border: 1px solid #991b1b;
        border-radius: 18px; 
        padding: 8px 5px;
        color: #991b1b;
        font-weight: 500; 
        outline: none;
    }

    .search-input::placeholder {
        color: #6b7280;
    }

    .movies-card {
    width: 11rem;
    height: 18rem;
    margin-bottom: 4px;
    background-color: #18181b;
    border-radius: 8px; 
    cursor: pointer;
    text-align: start;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: transform 0.4s ease, background-color 0.6s, box-shadow 0.4s; 
    }

    .movies-card:hover {
        transform: scale(1.05); 
        background-color: black; 
        box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
    }

    .about-movies {
        color: white;
    }

    .movie-img {
        width: 130px;
        object-position: center;
        border-radius: 4px;
    }

    .movie-name {
    font-size: 18px;
    margin: 5px 0;
    color: white;
    font-weight: bolder;
    overflow: hidden;
    white-space: nowrap;
    display: inline-block;
    width: 130px;
}

    .detail {
        display: flex;
        justify-content: space-between;
    }

    .detail-duration {
        font-weight: 400;
    }

    .detail-genre {
        color: #991b1b;
        font-weight: bold;
    }

</style>
