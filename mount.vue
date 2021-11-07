<template>
    <div>
        <h1>{{name}}</h1>
    </div>
</template>

<script>
    export default {
        name:'mount',
        data() {
            return {
                name: 'Mount'
            }
        },
        beforeMount()
        {
            console.warn("beforemount", this.$el)
        },
        mounted()
        {
            this.mount
            console.warn("mounted", this.$el)
        }
    }
</script>