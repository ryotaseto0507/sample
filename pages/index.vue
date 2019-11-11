<template>
  <div>
    <h1>Welcome!</h1>
    <NLink to="/about">
      About page
    </Nlink>
    <ul>
      <li v-for="post in $store.state.posts" v-bind:key="post.id">
        <a :href="'/posts/'+post.id">
          {{post.id}}
        </a>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  head: {
    title: 'Home page'
  },
}
</script>