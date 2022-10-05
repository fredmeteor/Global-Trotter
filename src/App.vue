<template>
  <div id="app">
<h1>

  {{name}}'s ToDo List
</h1>
  </div>

  <div class="container-fluid p-4">
  <div class="row">
  <div class="col font-weight-bold">Task </div>
  <div class="col-2 font-weight-bold">Done </div>
  <div class="row" v-for="t in tasks" v-bind:key="t.action">

    <div class="col">{{t.action}} </div>
  <div class="col-2"><input type="checkbox" v-model="t.done" class="form-check-input">{{t.done}} 

   <!-- <input type="checkbox" v-model="t.done" class="form-check-input"> -->
  </div>
  </div>
</div>
    </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',

  data(){

    return{

      name:"Pizza",

      tasks:[{action: "Buy Flowers",done:false},
              { action: "Get Shoes",done:false},
              { action: "Collect Tickets",done:true},

               {action: "Call Sumaya",done:true},
      
      ]
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
</style>
