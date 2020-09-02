<template>
  <v-card
    :loading="loading"
  >
    <v-img
      height="250"
      src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
    ></v-img>
     <v-row justify="space-around">

    <v-avatar color="indigo">
      <v-icon dark>mdi-account-circle</v-icon>
    </v-avatar>

    <v-avatar>
      <img
        src="https://cdn.vuetifyjs.com/images/john.jpg"
        alt="John"
      >
    </v-avatar>

    <!-- <v-avatar color="red">
      <span class="white--text headline">CJ</span>
    </v-avatar> -->

  </v-row>

    <v-card-title>Ruto Dc</v-card-title>

    <v-card-text>
      <v-row
        align="center"
        class="mx-0"
      >
        <v-rating
          :value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="grey--text ml-4">4.5</div>
      </v-row>

      <div class="my-4 subtitle-1">
        • About me
      </div>

      <div>I am a system admin and ICT consultant and trainer.</div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>

    <v-card-title>Hobbies</v-card-title>

    <v-card-text>
      <v-chip-group
        v-model="selection"
        active-class="deep-purple accent-4 white--text"
        column
      >
        <v-chip>coding</v-chip>

        <v-chip>travelling</v-chip>

        <v-chip>socializing</v-chip>

        <v-chip>reading</v-chip>
      </v-chip-group>
    </v-card-text>

    <v-card-actions>
      <v-btn
        color="deep-purple lighten-2"
        text
        @click="reserve"
      >
        Follow
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      loading: false,
      selection: 1,
    }),

    methods: {
      reserve () {
        this.loading = true

        setTimeout(() => (this.loading = false), 2000)
      },
    },
  }
</script>