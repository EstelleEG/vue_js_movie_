<template>
  <div>
    <nav>
      <!-- <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/films">Films</router-link>-->
      <div class="topnav">
        <ul class="mymenu">
          <li v-for="(menu, idx) in menuLinks" :key="idx">
            <!-- <router-link :to="{name:'home'}">Home</router-link> -->
            <router-link :to="{ name: menu.routeName }">{{ menu.label }}</router-link>
          </li>
        </ul>
      </div>

    </nav>
  </div>
</template>

<script>
export default {
  name: 'NavComp',
  data: () => ({
    menuLinks: [
      {
        routeName: 'home',
        label: 'Home'
      },
      {
        routeName: 'about',
        label: 'About us'
      },
      {
        routeName: 'films',
        label: 'Films'
      },
    ]
  })
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
