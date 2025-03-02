<script>
export default {
  data() {
    return {
      books: [
        {
          name: "Harry Potter",
          author: "J.K. Rowling",
          genre: "Fantasy",
          price: 2035,
        },
        {
          name: "The Hobbit",
          author: "J.R.R. Tolkien",
          genre: "Fantasy",
          price: 1500,
        },
        {
          name: "1984 Harry Porter",
          author: "George Orwell",
          genre: "Dystopian",
          price: 1000,
        },
      ],
      Writer:"MHA",
    };
  },
};
</script>

<template>
  <!-- List rendering -->
  <div class="books-list ">
    <div class="card" v-for="(book,index) in books">
        <p style="background-color: aquamarine;">Books No.{{ index + 1}}</p>
        <span>{{ Writer }}</span>
      <h1>{{ book.name }}</h1>
      <h2>{{ book.author }}</h2>
      <h3>{{ book.genre }}</h3>
      <h3>{{ book.price }}</h3>
      <button>Buy</button>
    </div>
  </div>
</template>

<style scoped>
.books-list {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}
.card {
  
  padding: 24px 32px;
  margin: 10px;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  background: tomato;
  gap: 10px;
}
h1,
h2,
h3 {
  color: black;
  font-size: 20px;
  font-weight:  500;
  line-height: 1.2em;
  margin: 0%;
}
</style>
