<template>
  <div id="app">
    <div id='links'>
      
      <router-link to="/listahorario">LISTA DE HORARIOS</router-link>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
      <router-link to="/">LOGIN</router-link>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
      <router-link to="/funcionario">FUNCIONARIO</router-link>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
      <router-link to='/servico'>SERVICO</router-link>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
      <a v-if="token" @click="logout">Logout</a>

    </div>
    <div id='teste'>
    <router-view/>
    </div>
  </div>
</template>

<script>
import {mapState, mapMutations} from 'vuex';

export default {
  name: 'App',
  computed:mapState(['token']),
  methods: {...mapMutations(['logout'])}
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  
}
#teste{
  
        width: 270px;
        border: 1px solid rgb(5, 31, 32);
        background-color: rgb(72, 196, 196);
        margin: auto;
        margin-top: 100px;
        padding: 20px;
        color: rgb(8, 8, 8)
}

</style>
