<template>
  <div>
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
  export default {
    name: "Booklist",
    data: function() {
      return {
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
</style>
