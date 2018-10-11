<template>
  <div>
  <select id="drop_1">
    <option value=""></option>
    <option :key="item.valor" :value="item.valor" v-for="item in itens">{{ item.descricao }}</option>
  </select>
  <select id="drop_2">
    <option value=""></option>
    <option :key="item.valor" :value="item.valor" v-for="item in itens">{{ item.descricao }}</option>
  </select>
  <select id="drop_3">
    <option value=""></option>
    <option :key="item.valor" :value="item.valor" v-for="item in itens">{{ item.descricao }}</option>
  </select>
  </div>
</template>

<script>
export default {
  props: {
    itens: Array
  }
}
</script>
