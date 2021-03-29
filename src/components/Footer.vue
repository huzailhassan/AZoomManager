<template>
  <v-footer
    dark
    padless
    app
    absolute
  >
    <v-card
      class="flex"
      flat
      tile
    >
      <v-card-title color="#242424">
           <v-btn
              color="#979797"
              fab
              x-small
              dark
            >
              <v-icon color="secondary">mdi-exclamation-thick</v-icon>
            </v-btn>
            
        <v-speed-dial
          class = "ma-auto"
          v-model="fab"
          :direction="direction"
          >
          <template v-slot:activator>
            <v-btn
              v-model="fab"
              color="primary"
              dark
              fab>
                
              <v-icon color="black" v-if="fab">
                mdi-close
              </v-icon>

              <v-icon color="black" v-else>
                mdi-plus
              </v-icon>

            </v-btn>
          </template>
        <v-dialog
          v-model="dialog"
          width="500"
        >
           <template v-slot:activator="{ on, attrs }">
          <v-btn
          v-bind="attrs"
          v-on="on"
            dark
            small
            rounded
            color="primary"
          >Add Category
          </v-btn>
           </template>
 <v-card>
        <v-card-title class="headline">
          Use Google's location service?
        </v-card-title>
        <v-card-text>Let Google help apps determine location. This means sending anonymous location data to Google, even when no apps are running.</v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="green darken-1"
            text
            @click="dialog = false"
          >
            Disagree
          </v-btn>
          <v-btn
            color="green darken-1"
            text
            @click="dialog = false"
          >
            Agree
          </v-btn>
        </v-card-actions>
      </v-card>
        </v-dialog>








          <v-btn
            dark
            small
            rounded
            color="primary"
          >Add Meeting
          </v-btn>
        </v-speed-dial>
      </v-card-title>
    </v-card>
  </v-footer>
</template>

<script>
import Modal from "./Modal"
  export default {
    data: () => ({
      components:{
        Modal
      },
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }),
  }
</script>