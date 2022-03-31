<template>
    <p v-if="custom_range > 67">Amas los {{what_to_love}}!</p>
    <p v-else-if="custom_range < 33">Odias a los {{what_to_love}}!</p>
    <p v-else>Te sientes normal con los {{what_to_love}}!</p>
    <input type="range" min="1" max="100" class="slider" id="custom_range" v-model="custom_range">
</template>

<script>

export default {
  name: 'LoveSlider',
  components: {
  },
  props :{
    what_to_love:String,
  },
  data(){
    return {
      custom_range :50,
    } 
  }
}
</script>

<style>

</style>
