<script >
export default {
    data() {
        return {
          counterStyle:'danger',
            count: 0, //This is call Data binding & Also call state
            isButtonDisabled: false,

        }
    },
    methods: {
        increase() {
            this.count++
            if(this.count > 10) {
                this.counterStyle = 'success',
                this.isButtonDisabled =true
            } 
        },
        decrease() {
            this.count--
            if(this.count < 5) {
                this.counterStyle = 'normal',
                this.isButtonDisabled =false
            } 
            
    },
    isDivisibleBy2(num){
      return num%2==0
    },
},
}
</script>

<template>
    <main class="container">
      <H2 v-bind="objectOfAttrs">Counter</H2>
      <div class="counter-wrapper">
        <button @click="increase" :disabled="isButtonDisabled">INCREASE </button>
      
        <H2 v-bind:class="counterStyle">{{ isDivisibleBy2(count) }}</H2>
        <button @click="decrease">DECREASE</button>
      </div>
    </main>
  
</template>

<style scoped>
main {
  text-align: center;
  margin-top: 50px;
}
.normal {
  color: #007f96;
}
.danger {
  color: #e94848;
}
.success {
  color: #00b679;
}
h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
}
.counter-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1rem;
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