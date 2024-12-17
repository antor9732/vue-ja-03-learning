<script>
import Counter from '@/components/Counter.vue'
import Header from '@/components/Header.vue';
import Footer from './components/Footer.vue';

export default{
  components:{
    Header,
    Counter,
    Footer,
  },
}
</script>

<template>
  <Header/>

  <Counter/>

  <Footer/>
</template>

<style>
* {
  margin: 0;
  box-sizing: border-box;
  padding: 0px;

}
</style>
