<template>
  <v-card
    color="rgba(255,255,255,.99)"
    width="60%"
    class="mt-12"
    min-width="300px"
  ><!-- rgba(255,255,255,.5) -->
    <v-card-title>
      <v-icon large left>chevron_right</v-icon>
      <span class="font-weight-light display-1 black--text">My albums</span>
    </v-card-title>
    <v-card-text>
      <v-list color="transparent">
        <v-list-group
          class="border-bottom block"
          color="inherit"
          v-for="songIndex in 3"
          :key="songIndex"
        >
          <template v-slot:activator>
            <v-list-item-avatar>
              <v-img
                max-width="40px"
                max-height="40px"
                :src="songs[songIndex - 1].img"
              />
            </v-list-item-avatar>
            <v-list-item-title class="headline black--text text-left">
              {{ songs[songIndex - 1].title }}
            </v-list-item-title>
          </template>

          <v-card class="overflow-y-auto box" color="transparent">
            <v-list-item-group v-model="songs[songIndex - 1].listenedSong">
              <v-list-item
                v-for="({ name, image, song }, i) in songs[songIndex - 1].array"
                :key="i"
                class="inherit"
                @click="musicEvent(song, songIndex, i)"
              >
                <v-list-item-avatar>
                  <v-img :src="image" />
                </v-list-item-avatar>
                <v-list-item-title
                  v-text="name"
                  class="subtitle-1 black--text text-left"
                />
              </v-list-item>
            </v-list-item-group>
          </v-card>
        </v-list-group>
      </v-list>
    </v-card-text>
  </v-card>
</template>

<script>
import { Howl } from "howler";
export default {
  name: "Albums",
  data() {
    return {
      sound: {
        song: {},
        songName: "",
        isSongActive: false
      },

      songs: [
        {
          listenedSong: -1,
          title: "Space",
          img: require("../../assets/Albums/space.png"),
          array: [
            {
              name: "Philae & Rosetta",
              image: require("../../assets/Albums/Space/PhilaeRosetta.png"),
              song: require("../../assets/AlbumsSongs/Space/PhilaeRosetta.mp3")
            },
            {
              name: "Saturn",
              image: require("../../assets/Albums/Space/Saturn.png"),
              song: require("../../assets/AlbumsSongs/Space/Saturn.mp3")
            },
            {
              name: "Sunset on Mars",
              image: require("../../assets/Albums/Space/SunsetOnMars.png"),
              song: require("../../assets/AlbumsSongs/Space/SunsetOnMars.mp3")
            },
            {
              name: "The Kuiper Belt",
              image: require("../../assets/Albums/Space/TheKuiperBelt.png"),
              song: require("../../assets/AlbumsSongs/Space/TheKuiperBelt.mp3")
            },
            {
              name: "Super Moon",
              image: require("../../assets/Albums/Space/SuperMoon.png"),
              song: require("../../assets/AlbumsSongs/Space/SuperMoon.mp3")
            },
            {
              name: "Orion fighting the scorpion",
              image: require("../../assets/Albums/Space/OrionFightingTheScorpion.png"),
              song: require("../../assets/AlbumsSongs/Space/OrionFightingTheScorpion.mp3")
            },
            {
              name: "Pluton & Charon",
              image: require("../../assets/Albums/Space/PlutonCharon.png"),
              song: require("../../assets/AlbumsSongs/Space/PlutonCharon.mp3")
            }
          ]
        },
        {
          listenedSong: -1,
          title: "Years",
          img: require("../../assets/Albums/years.png"),
          array: [
            {
              name: "January",
              image: require("../../assets/Albums/Years/January.png"),
              song: require("../../assets/AlbumsSongs/Years/January.mp3")
            },
            {
              name: "February",
              image: require("../../assets/Albums/Years/February.png"),
              song: require("../../assets/AlbumsSongs/Years/February.mp3")
            },
            {
              name: "March",
              image: require("../../assets/Albums/Years/March.png"),
              song: require("../../assets/AlbumsSongs/Years/March.mp3")
            },
            {
              name: "April",
              image: require("../../assets/Albums/Years/April.png"),
              song: require("../../assets/AlbumsSongs/Years/April.mp3")
            },
            {
              name: "May",
              image: require("../../assets/Albums/Years/May.png"),
              song: require("../../assets/AlbumsSongs/Years/May.mp3")
            },
            {
              name: "June",
              image: require("../../assets/Albums/Years/June.png"),
              song: require("../../assets/AlbumsSongs/Years/June.mp3")
            },
            {
              name: "July",
              image: require("../../assets/Albums/Years/July.png"),
              song: require("../../assets/AlbumsSongs/Years/July.mp3")
            },
            {
              name: "August",
              image: require("../../assets/Albums/Years/August.png"),
              song: require("../../assets/AlbumsSongs/Years/August.mp3")
            },
            {
              name: "September",
              //TODO: add September song!
              image: require("../../assets/Albums/Years/September.png"),
              song: require("../../assets/AlbumsSongs/Years/August.mp3")
              //image: require("../../assets/Albums/Years/September.png"),
              //song: require("../../assets/AlbumsSongs/Years/September.mp3")
            },
            {
              name: "October",
              image: require("../../assets/Albums/Years/October.png"),
              song: require("../../assets/AlbumsSongs/Years/October.mp3")
            },
            {
              name: "November",
              image: require("../../assets/Albums/Years/November.png"),
              song: require("../../assets/AlbumsSongs/Years/November.mp3")
            },
            {
              name: "December",
              image: require("../../assets/Albums/Years/December.png"),
              song: require("../../assets/AlbumsSongs/Years/December.mp3")
            }
          ]
        },
        {
          listenedSong: -1,
          title: "Reverse",
          img: require("../../assets/Albums/versus.png"),
          array: [
            {
              name: "Old & Young (47)",
              image: require("../../assets/Albums/Versus/Old&Young.png"),
              song: require("../../assets/AlbumsSongs/Versus/Old&Young.mp3")
            },
            {
              name: "South & North",
              image: require("../../assets/Albums/Versus/South&North.png"),
              song: require("../../assets/AlbumsSongs/Versus/South&North.mp3")
            },
            {
              name: "White & Black",
              image: require("../../assets/Albums/Versus/White&Black.png"),
              song: require("../../assets/AlbumsSongs/Versus/White&Black.mp3")
            },
            {
              name: "Far & Close to me (Ker Lann)",
              image: require("../../assets/Albums/Versus/Far&CloseToMe.png"),
              song: require("../../assets/AlbumsSongs/Versus/Far&CloseToMe.mp3")
            },
            {
              name: "Right & Wrong",
              image: require("../../assets/Albums/Versus/Right&Wrong.png"),
              song: require("../../assets/AlbumsSongs/Versus/Right&Wrong.mp3")
            },
            {
              name: "Life & Death",
              image: require("../../assets/Albums/Versus/Life&Death.png"),
              song: require("../../assets/AlbumsSongs/Versus/Life&Death.mp3")
            }
          ]
        }
      ]
    };
  },
  methods: {
    clear() {
      this.songs.forEach((_, i) => {
        this.songs[i].listenedSong = -1;
      });
    },
    musicEvent(song, albumIndex, songIndex) {
      this.clear();

      this.songs[albumIndex - 1].listenedSong = songIndex;

      if (this.sound.isSongActive === false) {
        this.listenMusic(song);
        this.sound.songName = song;
        this.sound.isSongActive = true;
      } else if (this.sound.songName === song) {
        this.stopMusic();
        this.sound.songName = "";
        this.sound.isSongActive = false;
      } else {
        this.stopMusic();
        this.listenMusic(song);
        this.sound.songName = song;
        this.sound.isSongActive = true;
      }
    },
    listenMusic(path) {
      this.sound.song = new Howl({
        src: [path],
        volume: 0.5
      });
      this.sound.song.play();
    },
    stopMusic() {
      this.sound.song.stop();
    }
  }
};
</script>

<style>
.border-bottom:hover {
  background-color: rgba(145, 145, 145, 0.1);
}

.border-bottom {
  border-bottom: 0.2px solid rgba(0, 0, 0, 0.2);
  box-shadow: 0.5px 0.5px 0px rgba(0, 0, 0, 0.2);
}

.block {
  padding-bottom: 10px;
  margin-bottom: 10px;
}

.box {
  max-height: 200px;
}

.inherit {
  color: inherit;
}

.text-left {
  text-align: left;
}
</style>
