<!-- date: 20-12-2024 
1. The same is true for class bindings
2. If your component has multiple root elements,
 you would need to define which element will receive this class.
 You can do this using the $attrs component property 
 3. Binding Inline Styles
 4. Binding to Arrays
 5. Reactivity Fundamentals
 6. Declaring Methods 
 7. Deep Reactivity 
 8. Reactive Proxy vs. Original
 -->
<script>
import Counter from "@/components/Counter.vue";
import Accordion from "@/components/Accordion.vue";

export default {
  components: { Accordion, Counter },
  // data() {
  //   return {
  //     // isActive: true,
  //     activeColor: 'red',
  //     fontSize: 48,
  //   //   styleObject: {
  //   //   color: 'green',
  //   //   fontSize: '48px'
  //   // }
  //   baseStyles: {
  //     color: 'green',
  //     fontSize: '32px'
  //   },
  //   overridingStyles: {
  //     backgroundColor: 'lightblue',
  //     fontSize: '62px'
  //   },

  //   };
  // },
  data() {
    return {
      obj: {
        nested: { count: 0 },
        arr: ["foo", "bar"],
      },
    };
  },

  methods: {
    mutateDeeply() {
      // these will work as expected.
      this.obj.nested.count++
      this.obj.arr.push('baz')
    }
  }
};
</script>

<template>
  <Counter />
  <!-- <Accordion class=" antor"/> -->
  <Accordion />
  <!-- <Accordion :class="{ antor: isActive }" /> -->
  <!-- <h3 :style="{ color: activeColor, fontSize: fontSize + 'px' }">Testing</h3> -->
  <!-- <h3 :style="[baseStyles, overridingStyles]">Testing</h3> -->

   <h3 @click="mutateDeeply()">{{obj.nested}}</h3>
   <h3>{{obj.arr}}</h3>
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
