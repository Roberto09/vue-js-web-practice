<template>
  <v-card
    class="mx-auto my-12"
    max-width="500"
  >
    <v-img
      height="250"
      v-bind:src="picture"
      cover
    ></v-img>

    <v-card-header>
      <v-card-header-text>
        <v-card-title>{{ picture_name}}</v-card-title>

      </v-card-header-text>
    </v-card-header>

  </v-card>
</template>

<script>

export default {
  name: 'CustomImg',
  components: {
  },
  props:{
    picture : String,
    picture_name : String,
  }
}
</script>

<style>

</style>