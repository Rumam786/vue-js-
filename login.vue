<template>
    <div>
        <p v-if="error.length">
            <b>please correct the following</b>
            <ul>
                <li v-for="e in error" v-bind:key="e.id">{{e.id}}</li>
            </ul>
        </p>
        <h1>Hello from login</h1>
        <form @submit="login">
        <input type="text" placeholder="enter name" v-model="name"><br><br>
        <input type="password" placeholder="enter password" v-model="password"><br><br>
        <button type="submit">login</button>
        </form>
    </div>
</template>

<script>
    export default {
        name:'login',
        data() {
            return {
                error: [],
                name: null,
                password: null
            }
        },
        methods: {
            login(e) {
                if(this.name && this.password)
                {
                    console.warn("no error")
                    return true
                }
                if(this.name)
                {
                    this.error.push("username is required");
                }
                if(this.password)
                {
                    this.error.push("password is required");
                }
                 console.warn("hello", this.error);
                e.preventDefault();         
            }
        },
    }
</script>