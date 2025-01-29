<script>
export default {
  data() {
    return {
      list: [],
      counter: 0,
      books: [
        {id: 1, title: "Harry Potter"},
        {id: 2, title: "Lord of the Rings"},
        {id: 3, title: "The Hobbit"},
        {id: 4, title: "The Chronicles of Narnia"},
      ],
    };
  },
  methods: {
    //API Call - this.list = updateValue[]
  
    isBookEvenOrOdd() {
      console.log("method called")
      return this.books.length % 2 === 0 ? "even" : "odd"
    },
    addMoreBooks() {
      this.computedIsBookEvenOrOdd = "even",
      this.books.push({
        id: this.books.length + 1,
        title: "New Book " + this.books.length + 1,

      })
    },
  },
  computed: {

    computedIsBookEvenOrOdd() {
      console.log("Computed called")
      return (this.books.length+this.counter) % 2 === 0 ? "even" : "odd"
    },
    computedIsBookEven() {
      this.books.push({
        id: this.books.length + 1,
        title: "New Book " + this.books.length + 1,
        
      });
    },
  },
  
}
</script>

<template>
  
 
    <h3> {{ books }} </h3>

    <h2>{{ isBookEvenOrOdd() }}</h2>
    <h2>{{ isBookEvenOrOdd() }}</h2>
    <h2>{{ isBookEvenOrOdd() }}</h2>
    <h2>{{ isBookEvenOrOdd() }}</h2>


    <h2>{{ computedIsBookEvenOrOdd }}</h2>
    <h2>{{ computedIsBookEvenOrOdd }}</h2>
    <h2>{{ computedIsBookEvenOrOdd }}</h2>
    <button @click="addMoreBooks">Add More Books</button>
    <button @click="counter++"> COUNT {{ counter }}</button>

</template>

<style></style>
