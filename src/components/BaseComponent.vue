<template>
  <div class="state">
    <h3>{{ counter }}</h3>
    <button @click="addOne">Add 1</button>
  </div>
</template>

<script>
export default {
  name: 'BaseComponent',
  methods: {
    addOne() {
      this.$store.state.counter ++;
    }
  },
  computed: {
    counter() {
      return this.$store.state.counter;
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
