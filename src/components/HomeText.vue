<template>
  <div>
    <p>{{ msgtext }}</p>
  </div>
  
</template>

<script>
export default {
  name: 'HomeText',
  props: { 
    msgtext: String,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
