<template>
  <v-card
    color="rgba(145,145,145,.3)"
    width="60%"
    class="mt-12"
    min-width="300px"
  >
    <v-card-title class="d-flex justify-center mr-5">
      <span>
        <v-icon large left>
          chevron_right
        </v-icon>
        <span class="font-weight-light headline">
          Comments
        </span>
      </span>
      <v-btn text icon>
        <v-icon>add</v-icon>
      </v-btn>
    </v-card-title>
    <v-card-text class="d-flex justify-end mr-5">
      <v-btn text icon>
        <v-icon>add</v-icon>
      </v-btn>
    </v-card-text>
    <v-card-text>
      <v-list color="transparent">
        <v-list-item v-for="({ pseudo, comment }, i) in comments" :key="i">
          <v-list-item-avatar color="grey darken-3">
            <v-img
              class="elevation-6"
              src="./../../assets/PhilippeFournierAvatar.jpg"
            />
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title class="subtitle-1">
              {{ pseudo }}
            </v-list-item-title>
          </v-list-item-content>
          <v-list-item-content>
            <v-list-item-title>
              {{ comment }}
            </v-list-item-title>
          </v-list-item-content>
          <v-btn text icon>
            <v-icon color="red darken-4">mdi-heart</v-icon>
          </v-btn>
        </v-list-item>
      </v-list>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: "Blog",
  data() {
    return {
      comments: []
    };
  },
  mounted() {
    this.fetchComments();
  },
  methods: {
    fetchComments() {
      this.comments = [
        {
          pseudo: "Mickaël",
          comment: "abcedf"
        },
        {
          pseudo: "Matthieu",
          comment: "ghijkl"
        },
        {
          pseudo: "Matthieu",
          comment: "mnopkrs"
        }
      ];
    }
  }
};
</script>

<style scoped></style>
