<template>
  <v-card
    class="mx-auto"
    max-width="500"
    tile
  >
    <v-list-item v-for="it in items" :key="it.id">
      <v-list-item-header>
        <v-list-item-title>{{it}}</v-list-item-title>
      </v-list-item-header>
    </v-list-item>
  </v-card>
</template>

<script>

export default {
  name: 'TextList',
  components: {
  },
  props :{
        items : Array,
        ordered : Boolean,
  },
}
</script>

<style>

</style>
