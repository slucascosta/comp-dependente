<template>
  <div>
    Pai: <SelectBox :itens="listaPai" @change.native="(e) => { dropSelecionado = e.target.id; valorPai = e.target.value }" /> |
    Filho: <SelectBox :itens="listaFilhos" />
    <br />
    {{ dropSelecionado }}
  </div>
</template>

<script>
import SelectBox from './components/SelectBox'
 
export default {
  components: { SelectBox },
    data () {
    return {
      listaPai: [
        { valor: 1, descricao: 'Item 1'},
        { valor: 2, descricao: 'Item 2'},
        { valor: 3, descricao: 'Item 3'}
      ],
      listaFilhoTodos: [
        { valor: 1, pai: 3, descricao: 'Item 1'},
        { valor: 2, pai: 3, descricao: 'Item 2'},
        { valor: 3, pai: 1, descricao: 'Item 3'}
      ],
      valorPai: null,
      dropSelecionado: null
    }
  },
  computed: {
    listaFilhos () {
      return this.listaFilhoTodos.filter(
        (x) => x.pai == this.valorPai);
    }
  }
}
</script>