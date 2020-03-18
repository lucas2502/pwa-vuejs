<template>
  <v-row justify="center">
    <v-col
      cols="6"
    >
        <v-img v-model="selected" max-width="100px" class="item-select" src="../assets/man.png" title="Selecionar Homem" @click.prevent="select('man')"></v-img>
    </v-col>

    <v-col
      cols="6"
    >
        <v-img v-model="selected" max-width="100px" class="item-select" src="../assets/woman.png" title="Selecionar mulher" @click.prevent="select('woman')"></v-img>
    </v-col>

  </v-row>
</template>

<script>
export default {
  data () {
    return {
      selected: null
    }
  },
  methods: {
    select (value) {
      this.selected = value
      this.$emit('select-sex', this.selected)
    }
  }
}
</script>

<style lang="scss" scoped>
.item-select {
  cursor: pointer;
  & :hover {
    opacity: 0.5
  }
}
</style>
