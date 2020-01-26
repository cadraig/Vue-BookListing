<template>
<li>{{book.title}}:{{book.author}}</li>
</template>

<script>
    export default {
        name: "BookItem",
        props: ["book"]
    }
</script>

<style scoped>
  li {
    display: block;
    margin: 0 10px;
  }
</style>

<!--
Adding Props to a Component
Inside of the BookItem's script tag, add an export default statement that contains the following:

a name property with a string value of BookItem
a props property with an array that contains one element, a string 'book'.

Using Interpolated Data in a Template
In BookItem.vue's <template> tag, add a single list item tag that contains the interpolated book.title, followed by a colon, followed by the interpolated book.author.

Moving Styles Between Components
Move the li rule from BookList.vue into BookItem.vue.
-->
