<template>
  <v-container class="pa-4 text-center">
    <v-row align="center" justify="center">
      <v-col cols="12">
        <v-img max-width="150px" src="../assets/logo.svg"></v-img>
      </v-col>
      <v-col cols="12">
        <h4>Alimentação Saudável</h4>
      </v-col>
    </v-row>
    <SelectSex @select-sex="selected"/>
  </v-container>
</template>

<script>
import SelectSex from '../components/SelectSex'

export default {
  components: {
    SelectSex
  },
  data () {
    return {
      valueSelected: null
    }
  },
  methos: {
    selected (e) {
      this.valueSelected = e
    }
  }
}
</script>

<style scoped>

</style>
