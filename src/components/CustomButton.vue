<template>
    <v-btn
      rounded="lg"
      color="primary"
      @click="on_click_func()"
    >
        {{text}}
    </v-btn>
</template>

<script>

export default {
  name: 'CustomButton',
  components: {
  },
  props :{
      on_click_func : Function,
      text : String,
  },
}
</script>

<style>

</style>
