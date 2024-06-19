<template>
  <form class="container">
    <input type="number" placeholder="Enter rate" required v-model="rate">
    <input type="number" placeholder="Enter hours" required v-model="hours">
    <label output></label>
    <button @click.prevent="calculateSalary">Calculate</button>
    <button>Clear</button>
    </form>
</template>

<script>
export default {
  name: 'App',
  components: {
    
  },
  data(){
    return{
      rate: '',
      hours: ''
    }
  },
 methods: {
     calculateSalary(){
      document.querySelector('[output]').textContent = this.rate * this.hours
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.container{
  display: grid;
  gap: .2rem;
  width: 30rem;
  margin-inline: auto;
  & input{
    text-align: center;
  }
}
</style>
