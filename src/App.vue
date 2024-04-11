<template>
  <input type="text">


</template>

<script>
export default {
  data() {
    return {
      post: []
    }
  },
  methods: {
    getPosts() {
      fetch('https://jsonplaceholder.typicode.com/posts')
        .then(response => response.json())
        .then(data => this.post = data)
        .then(data => console.log(data))

      
    }
  }
}
</script>