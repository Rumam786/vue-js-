<template>
<div>
    <input type="text" placeholder="enter your name" v-model="signup.username" /><br><br>
    <input type="text" placeholder="enter password" v-model="signup.password" /><br><br>
    <p>Choose Hoobies</p>
    <input type="checkbox" id="cricket" value="cricket" v-model="signup.hoobies" />
    <label for="cricket"> Cricket
    </label>
    <input type="checkbox" id="football" value="football" v-model="signup.hoobies" />
    <label for="football"> Football
    </label>
    <br><br>
    <p>Choose Gender</p>
    <input type="radio" id="male" value="male" v-model="signup.gender" />
    <label for="male"> Male
    </label>
    <input type="radio" id="female" value="female" v-model="signup.gender" />
    <label for="female"> Female
    </label><br><br>
    <button v-on:click="signupUser">signup</button>
</div>
</template>

<script>
export default {
    name: 'signup',
    data() {
        return {
            signup: {
                username: null,
                password: null,
                hoobies: [],
                gender: null
            }
        }
    },
    methods: {
        signupUser() {
            console.warn(this.signup)
        }
    },
}
</script>
