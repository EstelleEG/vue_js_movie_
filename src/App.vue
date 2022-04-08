<template>
  <div id="app">
    <NavComp />

    <main>
      <router-view />
    </main>
    
  </div>
</template>


<script>
import NavComp from '@/components/NavComp.vue'


export default {
  name: 'App',
  components: {
    NavComp,
  }
}
</script>

<style>
/* style du nav */

*{
  margin:0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

main{
  padding-top: 5rem;
}

main p{
  color:#04AA6D;
  font-size: 1.5rem;
}

.topnav {
  background-color: #333;
  overflow: hidden;
  padding-top: 1rem;
  padding-bottom: 1rem;
}


.topnav a {
  float: left;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

.topnav a:hover {
  background-color: #ddd;
  color: black;
}


.topnav a.active {
  background-color: #04AA6D;
  color: white;
}

ul {
  list-style-type: none;
}
</style>
