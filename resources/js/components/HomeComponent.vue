<template>
  <div class="main">

        <div v-for="(posts, index) in posts" :key="index" class="card">
            <h1>{{posts.title}}</h1>
            <p>{{posts.content}}</p>
        </div>
  </div>
</template>

<script>
import Axios from 'axios';

export default {
    name: 'HomeComponent',
    data(){
        return {
            posts: []
        }

    
    },
    mounted() {
        this.getData();
    },
    methods: {

        getData() {
            
            axios.get('/api/posts').then( resolve => {

                this.posts = resolve.data.results
            }
            )
            
        }
    }
}
</script>

<style>

</style>