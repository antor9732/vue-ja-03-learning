<script>
export default {
    data () {
        return {
            error: {
                name: null,
                email: null,
                password: null,
            },
        }
    },
    methods: {
        validateForm() {
            this.error.name = 'Invalid Name';
            this.error.email = 'Invalid Email';
            this.error.password = 'Incorrect Password';
            
    }
}
}
</script>

<template>
<form action="">
    <div class="form-group">
        <label for="name">Name:</label>
        <input type="text" name="name" id="name" placeholder="Enter your name">
        <div v-show="error.name">{{ error.name }}</div>
    </div>
    <div class="form-group">
        <label for="email">Email</label>
        <input type="text" name="email" id="email" placeholder="Enter your email">
        <div v-show="error.email">{{ error.email }}</div>

    </div>
    <div class="form-group">
        <label for="password">Password</label>
        <input type="password" name="password" id="password" placeholder="Enter your password">
        <div v-show="error.password">{{ error.password }}</div>

    </div>
    
    <button type="button" @click="validateForm" >SUBMIT</button>
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
