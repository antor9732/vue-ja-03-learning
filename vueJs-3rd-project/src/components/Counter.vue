<script>
export default {
  data() {
    return {
      count: 0, // this is the data property
      // isActive: true,
      // hasError: true,
      classObject: {
        'default-heading': true,
        "bg-danger": false,
      },
    };
  },
  methods: {
    increase() {
      this.count++;
      if (this.count > 0) {
        this.classObject["default-heading"] = false;
        this.classObject["bg-danger"] = false;
        // this.isActive = false;
        // this.hasError = false;
      }
    },
    decrease() {
      this.count--;
      if (this.count < 0) {
        this.classObject["default-heading"] = true;
        this.classObject["bg-danger"] = true;
        // this.isActive = true;
        // this.hasError = true;
      }
    },
  },
};
</script>

<template>
  <main class="container">
    <h1>Counter</h1>
    <div class="counter-wrapper">
      <button @click="increase">INCREASE</button>

      <h1
        class="static"
       :class="classObject"
      >
        {{ count }}
      </h1>

      <button @click="decrease">DECREASE</button>
    </div>
  </main>
</template>

<style scoped>
main {
  text-align: center;
  margin-top: 50px;
}

h1 {
  font-size: 3rem;
}
.counter-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1rem;
}
.default {
  color: red;
}
.bg-danger {
  background-color: royalblue;
}
.static {
  font-size: 3rem;
  font-weight: bold;
  align-items: center;
  justify-items: center;
}
button {
  font-weight: bold;
  font-size: 1.5rem;
  padding: 1rem 2rem;
  border-radius: 5px;
  background-color: rgb(255, 255, 255);
  border: 1px solid rgb(0, 0, 0);
}
</style>
