<template>
    <div class="user-container">
        <div class="profile-information" v-if="firstName.length > 0">
            <img :src="img" :alt="`${firstName} ${lastName}`">
            <h1>{{ firstName }}</h1>
            <h3>Email: {{ email }}</h3>
        </div>
        <div v-else><b>Click the button to display users.</b></div> <br>
        <Button v-on:click="generateUsers()" text="Start generating users" />
    </div>
</template>

<script>
import Button from './Button.vue'
export default{
    name: 'randomusers',
    data(){
        return {
            firstName: '',
            lastName: '',
            img: '',
            email: ''
        }
    },
    components: {
        Button,
    },
    methods: {
        async generateUsers(){
            const data = await fetch('https://randomuser.me/api')
            const { results } = await data.json()
            results.map((item) => {
                this.firstName = item.name.first
                this.lastName = item.name.last
                this.img = item.picture.large
                this.email = item.email
            })
        }
    }
}
</script>

<style scoped>

</style>