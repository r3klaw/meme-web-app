<template>
  <v-card
    class="mx-auto"
    
  >
    <v-container fluid>
      <v-row dense>
        <v-col
          v-for="card in cards"
          :key="card.title"
          :cols="card.flex"
        >
          <v-card>
            <v-card-actions> 
              {{card.title}}
              <v-spacer></v-spacer>
              <v-btn icon>
                <v-icon>mdi-account-plus-outline</v-icon>
              </v-btn>
            </v-card-actions>
            <v-img
              :src="card.src"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="200px"
            >
              <!-- <v-card-title v-text="card.title"></v-card-title> -->
            </v-img>

            <v-card-actions> 
              <v-spacer></v-spacer>
              <v-btn icon @click="likes">
                <v-icon>mdi-thumb-up-outline</v-icon>
              </v-btn>
              {{ like }}
              <v-spacer></v-spacer>
              <v-btn icon @click="dislikes">
                <v-icon>mdi-thumb-down-outline</v-icon>
              </v-btn>
              {{ dislike }}
              <v-spacer></v-spacer>
              <v-btn icon v-model="comments">
                <v-icon>mdi-chat-plus-outline</v-icon>
              </v-btn>
              {{ comments }}
              <v-spacer></v-spacer>
              <v-btn icon>
                <v-icon>mdi-arrow-down-bold-box-outline</v-icon>
              </v-btn>
              <v-spacer></v-spacer>
              <v-btn icon>
                <v-icon>mdi-share-variant</v-icon>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>

<script>
import comment from "~/components/comments";
  export default {
    components: {
    comment
  },
    data: () => ({
      cards: [
        { title: 'Pre-fab homes', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg'},
        { title: 'Favorite road trips', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg'},
        { title: 'Best airlines', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg'},
        { title: 'Pre-fab homes', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg'},
        { title: 'Favorite road trips', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg'},
        { title: 'Best airlines', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg'},
      ],
      like: 0,
      dislike: 0,
      comments: 50
    }),
    methods: {
    dislikes: function() {
      this.dislike++;
    },
    likes: function() {
      this.like++;
    }
    }
  }
</script>