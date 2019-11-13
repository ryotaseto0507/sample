<template>
  <div>
    <h1>Welcome!</h1>
    <NLink to="/about">
      About page
    </NLink>
    <ul>
      <li v-for="post in posts" v-bind:key="post.id">
        <NLink :to="`/posts/${post.id}`">
          {{post.title}}
        </NLink>
      </li>
    </ul>
    <NLink to="/new">
      Add New Post
    </NLink>
  </div>
</template>
<script>
export default {
  head: {
    title: 'Home page'
  },
  computed: {
    posts(){
      return this.$store.getters.posts
    },
  },
  methods: {
    }
  
}
</script>