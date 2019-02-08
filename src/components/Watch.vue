<template>
  <div class="">
    <p>{{ message }}</p>
    <p><input type="text" v-model="message" /></p>
    <pre>{{$data}}</pre>
  </div>
</template>

<script>
export default {
  name: "Watch",
  data() {
    return {
      message: "Vue.js"
    };
  },
  watch: {
    message: function(newValue, oldValue) {
      console.log("new: %s, old: %s", newValue, oldValue);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
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
pre {
  text-align: left;
}
</style>
