<script>
    import axios from 'axios'
    export default {
        name: 'search',
        data () {
            return {
                query: '',
                results: ''
            }
        },
        methods: {
        getResult(query) {
                axios.get('https://api.themoviedb.org/3/search/movie?api_key9cba81332618f150ad721b1be81a9d39query=' + query).then(response => { this.results = response.data.results })
                console.log(this.results)
                //console.log(query); 
            }
        }
    }
</script>


<template>
  <div class="greetings">
    <h1 class="green">Search Movies!</h1>
    <h3>
        <br>
        <input type='text' v-model='query' @keyup='getResult(query)'>
        <br>
        <button type="submit">Search Movies</button>
        <h2>{{ query }}</h2>
    </h3>
    <br>
    <div>
    <div>
        <div v-for='result in results' :key='result.id'>
            <p>{{result.title}}</p>
            <img v-bind:src="'http://image.tmdb.org/t/p/w500/' +    result.poster_path" width='100px'>
        </div>
    </div>
  </div>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
