<template>
   <div class="header">
       <ul>
        <li v-for="(posts, index) in menu" :key="index"><a :href="posts.link">{{posts.name}}</a></li>
       </ul>
       
   </div>
</template>

<script>

export default {
    name: 'HeaderComponent',
    data(){

        return {
            menu: [
                {
                    name: 'Home',
                    link: '#'
                },
                {
                    name: 'Blog',
                    link: '#'
                },
                {
                    name: 'Contacts',
                    link: '#'
                },
            ]
        }
    }
}
</script>

<style>

</style>