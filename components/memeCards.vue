<template>
  <v-bottom-navigation
    :value="activeBtn"
    grow
    color="dark"
    dark
  >
    <v-btn>
      <v-icon>mdi-home</v-icon>
    </v-btn>
    <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
    <v-btn>
      <v-icon>mdi-plus-box-outline</v-icon>
    </v-btn>
    <v-btn>
      <v-icon>mdi-bell</v-icon>
    </v-btn>
    <v-btn>
      <v-icon>mdi-account-circle</v-icon>
    </v-btn>
  </v-bottom-navigation>
</template>

<script>
  export default {
    data () {
      return {
        activeBtn: 1,
      }
    },
  }
</script>