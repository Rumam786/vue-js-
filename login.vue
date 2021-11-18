<template>
    <div>
        <h1>Post component</h1>
        <div>
            <table border="2px">
                <tr>
                    <td>ID</td>
                    <td>Username</td>
                    <td>Name</td>
                    <td>Email</td>
                    <td>Webiste</td>
                    <td>Phone</td>
                </tr>
                 <tr v-for="item in list" v-bind:key="item.id">
                     <td>{{item.id}}</td>
                     <td>{{item.username}}</td>
                    <td>{{item.name}}</td>
                    <td>{{item.email}}</td>
                    <td>{{item.website}}</td>
                    <td>{{item.phone}}</td>
                    <td><button v-on:click="deleteUser(user.id)">Delete</button></td>
                </tr>
            </table>
        </div><br><br>
        <router-link to="/">Go TO Home</router-link>
    </div>
</template>

<script>
import Vue from 'vue';
import VueAxios from 'vue-axios';
import axios from 'axios';
Vue.use(VueAxios,axios)
    export default {
        name:'users',
        data() {
            return {
                users: null
            }
        },
        methods: {
            getusers() {
                this.axios.get('https://jsonplaceholder.typicode.com/users').then((result)=>{
                    console.warn(result)
                    this.users=result.data
                })
            },
            deleteUser(id)
            {
                this.axios.delete('https://jsonplaceholder.typicode.com/users/'+id).then((result)=>{
                    console.warn(result)
                    this.users=result.data
                })    
            }
        }
    }
</script>