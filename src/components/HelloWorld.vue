<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <div>
      <label for="goal">Goal</label>
      <input type="text" id="goal" v-model="enteredValue">
      <button v-on:click="addGoal">Add Goal</button>
    </div>
    <ul>
      <li v-for="goal in goals" v-bind:key="goal">{{ goal }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      goals: [],
      enteredValue: ''
    };
  },
  methods: {
    addGoal() {
      this.goals.push(this.enteredValue)
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
