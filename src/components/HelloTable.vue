<template>
  <table>
    <tr v-for="index in rows" :key="index">
      <td v-for="j in cols" :key="j">
        {{j}}
      </td>
    </tr>
  </table>
</template>

<script>
export default {
  name: "HelloTable",
  data(){
    return {
      rows:25,
      cols:16,
    }
  },
}
</script>

<style scoped>

table, tr, td{
  border: 1px solid black;
  border-collapse: collapse;
}

</style>