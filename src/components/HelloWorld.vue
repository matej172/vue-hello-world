<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>{{ poznamka }}</h2>

    <span>{{ cislo }}</span>

    <div><span>
      Meno je {{user.name}} {{user.surname}}
    </span></div>

    <ul>
      <li v-for="(item, index) in pole" v-bind:key="index">
        {{index+1}}. {{item}}
      </li>
    </ul>

    <div v-if="cislo > 10">
      <h3>Toto je vygenerovane div</h3>
    </div>

    <div v-html="rawHtml"></div>

    <button @click="incrementCislo">Inkrementuj</button>
    <div>
      <label for="test-input">Hodnota čísla:
        <input v-model="cislo"  id="test-input" type="number">
      </label>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    poznamka: String,
  },
  data() {
    return {
      cislo: 15,
      pole: ['blue', 'red', 'yellow'],
      rawHtml: "<b>Toto je bold</b>",
      user:{
        name: "Matej",
        surname: "Rábek",
      }
    }
  },
  methods: {
    sucet(scitanec1, scitanec2){
      return scitanec1 + scitanec2;
    },
    incrementCislo(){
      this.cislo++;
    }
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
