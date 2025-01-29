<script>
export default {
    data () {
        return {
            step : 1,
        }
    },
    methods: {
        handleNextButton() {
            if(this.step < 3){
                this.step++
            }
        },
        handleBackButton() {
            if(this.step > 1){
                this.step--
            }
        },
},
}
</script>

<template>
<form action="">
    <div v-show="step === 1" class="form-group">
        <label for="name">Name:</label>
        <input type="text" name="name" id="name" placeholder="Enter your name">
    </div>
    <div v-show="step === 2" class="form-group">
        <label for="email">Email</label>
        <input type="text" name="email" id="email" placeholder="Enter your email">

    </div>
    <div v-show="step === 3" class="form-group">
        <label for="password">Password</label>
        <input type="text" name="password" id="password" placeholder="Enter your password">

    </div>
    
    <button type="button" @click="handleBackButton" v-show="step > 1">BACK</button>
    <button type="button" @click="handleNextButton" >
        {{ step <= 2 ?  'Next' : 'Submit' }}
    </button>
</form>
</template>

<style scoped>
.form-group{
    display: flex;
    flex-direction: column;
    gap: 10px;
    margin: 10px 0;
}
</style>
