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
      Writer: "MHA",

      //Example-2
      parentMessage: "Parent",
      items: [
        { 
        message: "Foo",
     }, 
     {
     message: "Bar",
     
    }],
    };
  },
};
</script>

<template>
  <!-- List rendering -->
  <div class="books-list">
    <div class="card" v-for="(book, index) in books">
      <p style="background-color: aquamarine;">Books No.{{ index + 1 }}</p>
      <span>{{ Writer }}</span>
      <h1>{{ book.name }}</h1>
      <h2>{{ book.author }}</h2>
      <h3>{{ book.genre }}</h3>
      <h3>{{ book.price }}</h3>
      <button>Buy</button>
    </div>
  </div>
  <!-- 1st example -->

  <div class="books-list-1">
    <li v-for="(item, index) in items">
      {{ parentMessage }} - {{ index }} - {{ item.message }}
    </li>
  </div>

  <br><br>
2nd example
<br><br>
  <li v-for="{ message } in items">
  {{ message }}
</li>
<br><br>
<!-- with index alias -->
<li v-for="({ message }, index) in items">
  {{ message }} {{ index }}
</li>



<br><br>
3rd Example
<br><br>
<h2>tag</h2>

</template>

<style scoped>
.books-list {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}
.books-list-1 {
  display: flex;
  flex-direction: column;
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
  font-weight: 500;
  line-height: 1.2em;
  margin: 0%;
}
</style>
