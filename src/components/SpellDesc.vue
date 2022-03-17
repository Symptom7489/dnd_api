<template>
<h1>Hello DnD</h1>
</template>

<script>
export default {
  name: "SpellDesc",
  props:['url'],
      data() {
    return {
    spells: [],
    };
  },
  mounted() {
 fetch(this.url)
    .then(res => res.json())
    .then(data => this.spells = data.results)
     .then(data => console.log(data.results))
    .catch(err => console.log(err.message))
  }
}
</script>

<style scoped>

</style>