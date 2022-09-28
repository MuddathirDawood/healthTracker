<template>
  <v-app :style="{background: $vuetify.theme.themes.light.background}">
    <v-layout row>
      <v-flex md8>
        <v-app :style="{background: $vuetify.theme.themes.dark.background}" class="rounded-tr-xl rounded-br-xl">
          <v-container>
            <v-row>
              <v-col cols="12" sm="12">
                <v-app-bar color="rgba(0,0,0,0)" flat class="mx-8 mb-8 mt-3">
                  <v-text-field prepend-icon="mdi-magnify" color="teal" placeholder="Search your symptoms" flat success>
                  </v-text-field>
                  <v-spacer></v-spacer>
                  <v-chip class="ma-2" color="white">
                    <v-icon left color="teal">mdi-clock-time-nine</v-icon> 
                    11:11 AM Today Sep,28
                  </v-chip>
                </v-app-bar>
              </v-col>
              <v-col cols="12" sm="12">
                <v-card class="mx-12 rounded-xl mt-15">
                  <v-list-item three line>
                    <v-list-item-content class="pa-10">
                      <v-list-item-title class="headline mb-1">
                        today <span class="teal--text">-10%</span> discount <br>
                        on lung examinations
                      </v-list-item-title>
                      <v-list-item-subtitle>
                        The package price includes: consultation <br>
                        of a pulmonologist, spirography, cardiogram <span class="teal--text">></span>
                      </v-list-item-subtitle>
                    </v-list-item-content>
                    <v-list-item-avatar tile size="150" class="pr-10">
                      <img src="https://i.postimg.cc/fTNkKfDw/TN-anatomy-lungs.jpg" alt="lungs">
                    </v-list-item-avatar>
                  </v-list-item>
                </v-card>
              </v-col>
              <v-col cols="12" sm="12">
                <v-card class="mx-12 rounded-xl mt-12">
                  <v-app-bar color="rgba(0,0,0,0)" flat class="ma-8">
                    <h5>Statistics of your health</h5>
                    <v-spacer></v-spacer>
                    <v-btn color="teal" text>
                      2019
                      <v-icon right>mdi-chevron-down</v-icon>
                    </v-btn>
                    <v-btn color="teal" rounded text depressed>Year</v-btn>
                    <v-btn text>Month</v-btn>
                  </v-app-bar>
                </v-card>
              </v-col>
            </v-row>
          </v-container>
        </v-app>
      </v-flex>
      <v-flex md3>
        <v-app :style="{background: $vuetify.theme.themes.light.background}">
          <v-container>
            
          </v-container>
        </v-app>
      </v-flex>
    </v-layout>
  </v-app>
</template>

<script>
  export default {
    name: 'Home',
    data(){
      return{
        width: 2,
        radius: 10,
        padding: 8,
        lineCap: 'round',
        value: [0,2,5,9,5,10,3,5,0,0,1,8,2,9,0],
        fill: false,
        type: 'trend',
        autoLineWidth: false
      }
    },
    computed:{
      theme(){
        return this.$vuetify.theme.dark ? 'dark' : 'light'
      }
    }
  }
</script>
