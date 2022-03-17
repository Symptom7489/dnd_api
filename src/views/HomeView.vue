<template>
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld :spells="spells"/>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  },
    data() {
    return {
    spells: [],
    };
  },
  mounted() {
 fetch('https://www.dnd5eapi.co/api/spells')
    .then(res => res.json())
    .then(data => this.spells = data.results)
     .then(data => console.log(this.spells))
    .catch(err => console.log(err.message))
  }
}
</script>




