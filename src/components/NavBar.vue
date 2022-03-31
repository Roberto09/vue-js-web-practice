<template>
      <v-navigation-drawer
        expand-on-hover
        rail
      >
        <v-list>
          <v-list-item
            title="My Pets App!"
          ></v-list-item>
        </v-list>


        <v-list density="compact" nav>
          <v-list-item title="Dog Fun Facts" href="https://www.britannica.com/animal/dog"></v-list-item>
          <v-list-item title="Cat Fun Facts" href="https://www.britannica.com/animal/cat"></v-list-item>
          <v-list-item title="Fish Fun Facts" href="https://www.britannica.com/animal/fish"></v-list-item>
        </v-list>
      </v-navigation-drawer>
</template>

<script>

export default {
  name: 'NavBar',
  components: {
  }
}
</script>

<style>

</style>