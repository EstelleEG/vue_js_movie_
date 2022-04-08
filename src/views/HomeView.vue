<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/cine.jpg">
    <HomeComp msg="Select your movie with the link below"/>

    <HomeText msgtext="Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s"/>

    

  </div>
</template>

<script>
// @ is an alias to /src
import HomeComp from '@/components/HomeComp.vue'
import HomeText from '@/components/HomeText.vue'


export default {
  name: 'HomeView',

  components: {
    HomeComp, 
    HomeText
  
  }
}
</script>
