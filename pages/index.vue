<template>
  <div>
    <h1>Welcome! Tokyo!</h1>
    <NLink to="/about">
      About page
    </Nlink>
    <br>
    <NLink to="/posts/balut">
      1
    </Nlink>
    <br>
    <NLink to="/posts/whereIsIt">
      2
    </NLink>
    <br>
    <NLink to="/posts/how">
      3
    </NLink>
  </div>
</template>
<script>
export default {
  head: {
    title: 'Home page'
  }
}
</script>