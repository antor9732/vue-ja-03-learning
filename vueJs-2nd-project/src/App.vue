<script>
import Counter from '@/components/Counter.vue'
import Header from '@/components/Header.vue';

export default{
  components:{
    Counter,
    Header,
  },
}
</script>

<template>
  <Header/>

  <counter/>
</template>

<style>
* {
  margin: 0;
  box-sizing: border-box;
  padding: 10px 10px;

}
</style>
