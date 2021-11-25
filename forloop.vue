<template>
<div>
    <h1>hello</h1>
    <table border="2px">
        <tr>
            <td>Id</td>
            <td>Name</td>
            <td>Email</td>
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
    name: 'home',
    data() {
        return {
            users: [{
                    id: 1,
                    name: 'peter',
                    email: 'peter@gmail.com'
                },
                {
                    id: 2,
                    name: 'bruce',
                    email: 'bruce@gmail.com'
                },
                {
                    id: 3,
                    name: 'tony',
                    email: 'tony@gmail.com'
                },
                {
                    id: 4,
                    name: 'sam',
                    email: 'sam@gmail.com'
                },
            ]
        }
    },
}
</script>

<style lang="scss" scoped>

</style>
