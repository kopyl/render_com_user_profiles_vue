<template>
    <h3>Users6:</h3>
    <User :username=username v-for="{username} of users" :key='username'/>
</template>

<script>
import User from './components/User.vue'

export default {
    name: 'App',

    data() {
        return {
            users: [],
            URLS: {
                usersAPI: 'http://185.178.46.211:90/users'
            }
        }
    },

    beforeMount: function() {
        this.getUsers()
    },

    methods: {

        async getUsers() {
            // let users = await fetch(this.URLS.usersAPI)
            // this.users = await users.json()

            console.log('RENDER_EXTERNAL_HOSTNAME', process.env.RENDER_EXTERNAL_HOSTNAME)
            // console.log(presets)
        }

    },
    
    components: {
        User
    }
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: left;
    color: #2c3e50;
    margin-top: 60px;
    margin-left: 2em
}
</style>
