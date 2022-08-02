<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <div>
      {{hello}}
    </div>
    <a :href="url">drive </a>
    <p>---------------------------------------------</p>

    <h1 class="class1">aaaaaaaaa</h1>
    <p>---------------------------------------------</p>
    <!-- Methodes -->
    <h4>{{counter}}</h4>
    <button @click="increase()">+</button>
    <button @click="decrease()">-</button>
<p>---------------------------------------------</p>

  <!-- boucle if -->
    <div v-if="gender === 'male'">male </div>
    <div v-else-if="gender === 'female'">female</div>
<p>---------------------------------------------</p>

    <!-- boucle for table-->
    <li v-for="e in etudiants" :key="e">
      {{e}}
    </li>
<p>---------------------------------------------</p>
    <!-- boucle for JSON -->
    <li v-for="e in employes" :key="e">
      {{e.name}}  :  {{e.age}}
    </li>

  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data(){
    return {
     hello:'hello Nour !! ',
     url:'https://drive.google.com/drive/shared-with-me',
     counter:0,
     gender:"male",
     etudiants:['aya','nour','maryem','hanin','ahmed','ilhem'],
     employes:[
      {"name":"aya","age":20},
      {"name":"nour","age":22},
      {"name":"ilhem","age":24},
     ]
    }
  },
  methods:{
increase(){
  this.counter++;
},

decrease(){
  this.counter--;
}
  }
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
.class1{
color:red;
}
</style>
