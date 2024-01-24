<script setup>
import { RouterLink} from 'vue-router'
</script>

<template>
  <div class="data">
    <p>Type in your data</p>
    <p></p>
    <input type="text" placeholder="Type in your name" v-model="name">
    <input type="number" v-bind:placeholder="text" v-model="age">
    <button v-on:click="greet(name,age)"> Calculate my max aerobic heart rate</button>
   </div>
 
 <br>
 <div>
  <p>{{name}} ,Type in your weight in kilograms:</p>
  <input
  type="number"
        v-model="modelValue"
    />
    <p>Your weight in pounds is {{modelValue===0?"":modelValue*2.204}}</p>
 </div>
 <RouterLink v-bind:to="link()">Click for good luck</RouterLink>
 
</template>


<script>
export default {
  
  data() {
    return {
      name:"",
      age:null ,
      modelValue:0,
      text:"Type in your age"
    };
  },
  methods: {
    greet: function (name,age) {
      // `this` inside methods point to the Vue instance
      let rate=180 - age;
      alert('Hello ' + name + ' your max aerobic heart rate is' + rate + '!')
     
    },
    link:function(){
      return "/motivation/"+this.name;
    }
  }
}
</script>


<style scoped>

input{
  margin: 5px;
}

.data{
 
  display: grid;
  width: 10%;
  
}
</style>