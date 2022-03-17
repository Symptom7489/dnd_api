<template>
<ul>
  <li v-for="spell in spells" :key="spell.index"  >
    {{ spell.name}}
    {{spell.url}}  <button @click="console.log(spell.url)"> URL TEST </button>
  </li>
</ul>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: ['spells'],
  data () {
    return {
  spellName: ' ',
    };
  },
  methods: {
   testSpell() {
      console.log(this.spells);
    }
  },
  computed: {

  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
