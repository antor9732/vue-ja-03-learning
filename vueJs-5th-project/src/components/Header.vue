<script>
export default {
  data() {
    return {
      isUserLoggedIn: false,
    };
  },
  methods: {
    SignIn() {
      this.isUserLoggedIn = true;
    },
    logOut() {
      this.isUserLoggedIn = false;
    },
  },
  mounted() {
    // this.isUserLoggedIn = !this.isUserLoggedIn;
    console.log('This component is mounted')
  }
};
</script>

<template>
  <header>
    <h1>My Todo List</h1>

    <div v-if="isUserLoggedIn">
        <h2>Profile</h2>
        <button @click="logOut">LOG OUT</button>
    </div>
    <div v-else>
        <button @click="SignIn">SIGN IN</button>
        <button>SIGN UP</button>
    </div>

  </header>
</template>

<style scoped></style>
