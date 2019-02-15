<template>
  <div>
    <header>
      <slot name="header"></slot>
      <h1>Project Header</h1>
    </header>
    <footer>
      <h4>Project Footer</h4>
      <slot name="footer" :nameInfo="name"></slot>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: { firstName: 'DAAAA', lastName: 'YAAAAA' },
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
