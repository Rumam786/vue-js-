<template>
    <div>
        <h1>employes list</h1>
        <div>
            <table border="2px">
                <tr>
                    <td>name</td>
                    <td>id</td>
                    <td>email</td>
                </tr>
                 <tr v-for="item in list" v-bind:key="item.id">
                    <td>{{item.name}}</td>
                    <td>{{item.id}}</td>
                    <td>{{item.email}}</td>
                </tr>
            </table>
        </div>
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
                list: undefined
            }
        },
        mounted()
        {
            Vue.axios.get('https://jsonplaceholder.typicode.com/users')
            .then(resp=>{
                this.list=resp.data
                console.warn(resp.data)
            })
        }
    }
</script>