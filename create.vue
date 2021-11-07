<template>
    <div>
        <h1>{{name}}</h1>
    </div>
</template>

<script>
    export default {
        name:'create',
        data() {
            return {
                name: 'Ruman'
            }
        },
         created()
        {

            console.warn("created", this.name="sukhera")
        },
        beforeCreate()
        {
            console.warn("beforecreate", this.name)
        }
    }
</script>