<template>
    <div>
        <h1 v-if="show">conditional rendering if condition</h1>
        <h1 v-else>conditional rendering else block</h1>
        <button v-on:click="display">toogle element</button>

    </div>
</template>

<script>
    export default {
        name:'conditions',
        data() {
            return {
                show: true
            }
        },
        methods: {
            display() {
                this.show=!this.show
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>