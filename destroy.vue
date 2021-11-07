<template>
<div>
    <h1>{{name}}</h1>
</div>
</template>

<script>
export default {
    name: 'Destroy',
    data() {
        return {
            name: 'Destroy'
        }
    },
    beforeDestroy() {
        alert("before")
        console.warn("before destroy")
    },
    destroyed() {
        alert("destroyed")
        console.warn("destroyed")
    }
}
</script>
