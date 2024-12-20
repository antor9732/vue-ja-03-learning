<!-- date: 20-12-2024 
1. The same is true for class bindings
2. If your component has multiple root elements,
 you would need to define which element will receive this class.
 You can do this using the $attrs component property 
 3. Binding Inline Styles
 4. Binding to Arrays
 -->
<script>
// import Counter from '@/components/Counter.vue';
import Accordion from '@/components/Accordion.vue';

export default{
  components:{ Accordion },
  data() {
    return {
      // isActive: true,
      activeColor: 'red',
      fontSize: 48,
    //   styleObject: {
    //   color: 'green',
    //   fontSize: '48px'
    // }
    baseStyles: {
      color: 'green',
      fontSize: '32px'
    },
    overridingStyles: {
      backgroundColor: 'lightblue',
      fontSize: '62px'
    },

    };
  },

};
</script>

<template>
  <!-- <Counter/> -->
  <!-- <Accordion class=" antor"/> -->
  <Accordion :class="{'antor' : isActive}"/>

  <!-- <h3 :style="{ color: activeColor, fontSize: fontSize + 'px' }">Testing</h3> -->
  <h3 :style="[baseStyles,overridingStyles]">Testing</h3>
</template>

<style>
* {
  margin: 0;
  box-sizing: border-box;
  padding: 0px;

}
/* .antor {
    display: block;
} */

.antor {
    display: none;
}
</style>
