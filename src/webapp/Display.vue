<template>
    <div>
      <ul v-for="movie in movies" :key="movie">
        <p>{{ movie }}</p>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        movies: [],
      };
    },
  
    methods: {
      async getData() {
        try {
          let response = await fetch("https://api.themoviedb.org/3/movie/550?api_key=9cba81332618f150ad721b1be81a9d39");
          this.movies = await response.json();;
        } catch (error) {
          console.log(error);
        }
      },
    },
  
    created() {
      this.getData();
    },
  };
  </script>