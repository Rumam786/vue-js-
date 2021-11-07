<template>
    <div>
        <h1>Array</h1>
        <table border="2px">
            <tr>
                <td>id</td>
                <td>name</td>
                <td>email</td>
            </tr>
             <tr v-for="user in users" :key="user.id">
                <td>{{user.id}}</td>
                <td>{{user.name}}</td>
                <td>{{user.email}}</td>
            </tr>
        </table>
    </div>
</template>

<script>
    export default {
        name:'array',
        data() {
            return {
                users:[
                    {id:1, name:'ruman', email:'ruman@gmail.com'},
                    {id:2, name:'usman', email:'usman@gmail.com'},
                    {id:3, name:'arslan', email:'arslan@gmail.com'}
                ]
            }
        },
    }
</script>