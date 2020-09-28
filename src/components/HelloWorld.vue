<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <strong>{{ count }}</strong>

    <div>
      <button @click="decrement">-</button>
      <button @click="increment">+</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: () => ({
    count: 0
  }),
  methods: {
    decrement() {
      if (this.count > 0) {
        this.count--
      }
    },
    increment() {
      this.count++
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
