<template>
  <div>
    <h1>Welcome!</h1>
    <i class="iconfont icon-changyongicon-"></i>
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
    <i class="iconfont icon-changyongicon-"></i>
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

<style>
   @import "//at.alicdn.com/t/font_1523487_auyvrjtr4yf.css"
</style>
