<template>
  <div>
    <h1>{{ title }}</h1>
    <ul>
      <!-- book-item v-for="book in books" v-bind:bookie="book" v-bind:key="book"></book-item -->
      <book-item v-for="book in books" :book="book"></book-item>
    </ul>
    <book-form @addBook='appendBook'></book-form>
  </div>
</template>

<!-- Back in BookList.vue's script tag, import BookForm from ./BookForm and add the BookForm component to the components object.  -->
<script>
  import BookItem from "./BookItem";
  import BookForm from "./BookForm";
  export default {
    name: "BookList",
    components: {BookItem},
    methods: {
      appendBook (bookTitle, bookAuthor) {
        this.books.push({ title: bookTitle, author: bookAuthor });
      }
    },
    data: function() {
      return {
        components: {
          BookItem,
          BookForm
        },
        books: [
            {title: 'Self-Reliance', author: 'Ralph Waldo Emerson'},
            {title: 'American Gods', author: 'Neil Gaiman'},
            {title: 'Amusing Ourselves to Death', author: 'Neil Postman'}
          ],
        title: "All Books"
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only-->
<style scoped>
  h1, h2 {
    font-weight: normal;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
</style>

<!--

-->
