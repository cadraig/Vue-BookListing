<template>
  <div>
    <h1>{{ title }}</h1>
    <ul>
      <li v-for="book in books">{{book.title}}:{{book.author}}</li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "BookList",
    data: function() {
      return {
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
    list-style: none;:wq
    padding: 0;
  }
  li {
    display: block;
    margin: 0 10px;
  }
</style>

<!--
In BookList.vue's template tag,
replace all three list item tags with a single list item tag that contains the interpolated book.title,
followed by a colon, followed by the interpolated book.author.

-->
