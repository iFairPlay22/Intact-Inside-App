<template>
    <v-carousel height="100%" hide-delimiters interval=10>
        <v-carousel-item v-for="(link, i) in links" :key="i" :src="link">
            <v-container grid-list-md class="container">
                <v-layout align-center justify-center space-around column fill-height>
                    <v-card color="rgba(145,145,145,.3)" width="60%">
                        <v-card-title>
                            <v-icon large left>
                                chevron_right
                            </v-icon>
                            <span class="font-weight-light headline">Intact Inside</span>
                        </v-card-title>
                        <v-card-text class="headline justify-center">
                            Every month is a new chance and a new hope! I hope you will enjoy my albums as much as I enjoyed releasing them.
                        </v-card-text>
                        <v-card-actions>
                            <v-list-item class="grow">
                                <v-list-item-avatar color="grey darken-3">
                                    <v-img class="elevation-6" src="./../../assets/PhilippeFournierAvatar.jpg" />
                                </v-list-item-avatar>
                                <v-list-item-content>
                                    <v-list-item-title class="subtitle-1">
                                        Philippe Fournier
                                    </v-list-item-title>
                                </v-list-item-content>
                                <v-row align="center" justify="end">
                                    <v-btn text icon>
                                        <v-icon color="red darken-4">mdi-heart</v-icon>
                                    </v-btn>
                                    <span class="subheading mr-2">256</span>
                                </v-row>
                            </v-list-item>
                        </v-card-actions>
                    </v-card>
                    <v-card color="rgba(145,145,145,.3)" width="60%" class="mt-12">
                        <v-card-title>
                            <v-icon large left>
                                chevron_right
                            </v-icon>
                            <span class="font-weight-light headline">
                              My albums
                            </span>
                        </v-card-title>
                        <v-card-text>
                            <v-row justify="center" class="mx-0 mt-2">
                                <v-expansion-panels accordion>
                                    <v-expansion-panel class="transparent mb-2">
                                        <v-expansion-panel-header class="title">
                                            <v-list-item-group class="d-flex justify-start">
                                                <v-list-item-avatar>
                                                    <v-img max-width="40px" max-height="40px" :src="yearsImg"></v-img>
                                                </v-list-item-avatar>
                                                <v-list-item-content>
                                                    <v-list-item-title>
                                                        Years
                                                    </v-list-item-title>
                                                </v-list-item-content>
                                            </v-list-item-group>
                                        </v-expansion-panel-header>
                                        <v-expansion-panel-content>
                                            <v-list color="transparent">
                                                <v-list-item v-for="({name, image}, i) in songs.years" :key="i">
                                                    <v-list-item-avatar>
                                                        <v-img :src="image"></v-img>
                                                    </v-list-item-avatar>
                                                    <v-list-item-content>
                                                        <v-list-item-title v-text="name"></v-list-item-title>
                                                    </v-list-item-content>
                                                    <v-btn text icon>
                                                        <v-icon color="red darken-4">mdi-heart</v-icon>
                                                    </v-btn>
                                                </v-list-item>
                                            </v-list>
                                        </v-expansion-panel-content>
                                    </v-expansion-panel>
                                    <v-expansion-panel class="transparent">
                                        <v-expansion-panel-header class="title">
                                            <v-list-item-group class="d-flex justify-start">
                                                <v-list-item-avatar>
                                                    <v-img max-width="40px" max-height="40px" :src="spaceImg"></v-img>
                                                </v-list-item-avatar>
                                                <v-list-item-content>
                                                    <v-list-item-title>
                                                        Space
                                                    </v-list-item-title>
                                                </v-list-item-content>
                                            </v-list-item-group>
                                        </v-expansion-panel-header>
                                        <v-expansion-panel-content>
                                            <v-list color="transparent">
                                                <v-list-item v-for="({name, image}, i) in songs.space" :key="i">
                                                    <v-list-item-avatar>
                                                        <v-img :src="image"></v-img>
                                                    </v-list-item-avatar>
                                                    <v-list-item-content>
                                                        <v-list-item-title v-text="name"></v-list-item-title>
                                                    </v-list-item-content>
                                                    <v-btn text icon>
                                                        <v-icon color="red darken-4">mdi-heart</v-icon>
                                                    </v-btn>
                                                </v-list-item>
                                            </v-list>
                                        </v-expansion-panel-content>
                                    </v-expansion-panel>
                                </v-expansion-panels>
                            </v-row>
                        </v-card-text>
                    </v-card>
                </v-layout>
            </v-container>
        </v-carousel-item>
    </v-carousel>
</template>

<script>
  export default {
    name: "Presentation",
    data() {
      return {
        links: [
          require('../../assets/Carousel/1.jpg'),
          require('../../assets/Carousel/2.jpg'),
          require('../../assets/Carousel/3.jpg'),
          require('../../assets/Carousel/4.jpg'),
          require('../../assets/Carousel/5.jpg')
        ],
        selectedSong: '',
        yearsImg: require('../../assets/Albums/years.jpg'),
        spaceImg: require('../../assets/Albums/space.jpg'),
        songs: {
          space: [
          {
           name: 'Philae & Rosetta', 
           image: require('../../assets/Albums/Space/PhilaeRosetta.jpg')
          },
          {
           name: 'Saturn',  
           image: require('../../assets/Albums/Space/Saturn.jpg')
          },
          {
           name: 'Sunset on Mars',
           image: require('../../assets/Albums/Space/SunsetOnMars.jpg')
          },
          {
           name: 'The Kuiper Belt',  
           image: require('../../assets/Albums/Space/TheKuiperBelt.jpg')
          },
          {
           name: 'SuperMoon',  
           image: require('../../assets/Albums/Space/SuperMoon.jpg')
          },
          {
           name: 'Orion fighting the scorpion',  
           image: require('../../assets/Albums/Space/OrionFightingTheScorpion.jpg')
          },
          {
           name: 'Pluton & Charon',  
           image: require('../../assets/Albums/Space/PlutonCharon.jpg')
          }
        ],
        years: [
          {
           name: 'January',  
           image: require('../../assets/Albums/Years/January.jpg')
          },
          {
           name: 'February',  
           image: require('../../assets/Albums/Years/February.jpg')
          },
          {
           name: 'March',  
           image: require('../../assets/Albums/Years/March.jpg')
          },
          {
           name: 'April',  
           image: require('../../assets/Albums/Years/April.jpg')
          },
          {
           name: 'May',  
           image: require('../../assets/Albums/Years/May.jpg')
          },
          {
           name: 'June',  
           image: require('../../assets/Albums/Years/June.jpg')
          },
          {
           name: 'July',  
           image: require('../../assets/Albums/Years/July.jpg')
          },
          {
           name: 'August',  
           image: require('../../assets/Albums/Years/August.jpg')
          },
          {
           name: 'September',  
           image: require('../../assets/Albums/Years/September.jpg')
          },
          {
           name: 'October',  
           image: require('../../assets/Albums/Years/October.jpg')
          },

          {
           name: 'November',  
           image: require('../../assets/Albums/Years/November.jpg')
          },

          {
           name: 'December',  
           image: require('../../assets/Albums/Years/December.jpg')
          }
        ]
        }
      }
    },
    methods: {
      
    }
  };
</script>

<style scoped>
  .container {
    margin-top: 200px;
  }

  .test {
    background-color: green;
  }
</style>