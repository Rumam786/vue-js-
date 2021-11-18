<template>
    <div>
        <input type="text" placeholder="enter your name" /><br><br>
        <input type="text" placeholder="enter password" /><br><br>
        <p>Choose Hoobies</p>
        <input type="checkbox" id="cricket" value="cricket"/>
        <label for="cricket"> Cricket
            </label>
             <input type="checkbox" id="football" value="football"/>
        <label for="football"> Football
            </label>
            <br><br>
            <p>Choose Gender</p>
             <input type="radio" id="male" value="male"/>
        <label for="male"> Male
            </label>
             <input type="radio" id="female" value="female"/>
        <label for="female"> Female
            </label>
    </div>
</template>

<script>
    export default {
        name:'signup'
    }
</script>

<style lang="scss" scoped>

</style>