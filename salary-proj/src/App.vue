<template>
<form class="container">
<input type="number" placeholder="Enter Your Rate" required v-model="rate">
<input type="number" placeholder="Enter Your Hours" required v-model="hours">
<label result readonly></label>
<button @click.prevent="calcSalary">Calulate</button>
<button>Clear</button>
</form>
</template>

<script>

export default {
  name: 'App',

  components: {

  },
  data() {
    return {
      rate: '',
      hours: ''
    }
  },


  methods: {
    calcSalary() {

      document.querySelector('[result]').textContent = 
      this.rate * this.hours
      
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
  & input {
    text-align: center;
  }
}

</style>
