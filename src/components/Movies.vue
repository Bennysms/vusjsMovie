<script setup>
    import {ref} from 'vue'
    const movies = ref([])
    const search = ref("")

    const SearchMovies = () =>{
        if (search.value !==""){
            fetch(`https://www.omdbapi.com/?apikey=97aa5456&s=${search.value}&plot=full`)
            .then(response => response.json())
            .then(data =>{
                console.log(data.Search);
                movies.value = data.Search;
                search.value="";
            })
        }
    }


</script>

<template>
<div class="max-w-7xl mx-auto px-4 py-6 bg-gray-300">
    <form @submit.prevent="SearchMovies()" class="flex gap-3 md:flex-row flex-col">
         <input type="search" placeholder="Trouvez vos filmes..." class="py-3 px-5 rounded-full text-gray-500 outline-none border-none" v-model="search">
         <input type="submit" value="Search" @click.prevent="SearchMovies()" class="py-3 px-5 rounded-full outline-none border-none cursor-pointer bg-[rgb(78,176,124)] text-white">
    </form>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 mt-5 gap-5">
        <div v-for="movie in movies" :key="movie.imdbID" class="relative h-[400px] w-full overflow-hidden shadow-2xl group">
            <img :src="movie.Poster" :alt="movie.Title" class="w-full h-full object-cover  hover:scale-125 transition-all duration-500 cursor-pointer">
            <div class="absolute -bottom-[100%] bg-[#ffffffa2] w-full p-4 backdrop-blur-sm group-hover:bottom-0 transition-all duration-500 ">
                <h1 class="font-bold text-md md:text-xl mb-2 text-green-900">{{movie.Title}}</h1>
                <div class="flex justify-between text-green-700 font-semibold text-sm md:text-md">
                    <p>Type : {{movie.Type}}</p>
                    <p>Année : {{movie.Year}}</p>
                </div>
            </div>
        </div>
    </div>
</div>
  
</template>

<style>

</style>