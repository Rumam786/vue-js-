<template>
<div>
    <form @submit="submitdata" method="post"></form>
    <input type="text" name="title" v-model="post.title" placeholder="title" /><br><br>
    <input type="text" name="author" v-model="post.body" placeholder="body" /><br><br>
    <button type="submit">post</button>
</div>
</template>

<script>
import Vue from 'vue'
import axios from 'axios'
import VueAxios from 'vue-axios'
Vue.use(VueAxios,axios)
export default {
    name: 'post',
    data() {
        return {
            post: {
                title: null,
                body: null
            }
        }
    },
    methods: {
        submitdata(e) {
            this.axios.post('https://jsonplaceholder.typicode.com/posts', this.post).then((result) => {
                    console.warn("result", result)
                    console.warn(this.post)
                })
                e.preventdefault();
            }
        }
    }
</script>
