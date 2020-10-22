<template>
  <table>
    <tr v-for="i in rows" :key="i">
      <td v-for="j in cols" :key="j">
        {{j}}
      </td>
    </tr>
  </table>
</template>

<script>
export default {
  name: "HelloTable",

  props:{
    rows: Number,
    cols: Number
  },
  mounted() {
    console.log(this.rows)
  }
}
</script>

<style scoped>

table, tr, td{
  border: 1px solid black;
  border-collapse: collapse;
}

</style>