<template>
  <v-dialog v-model="dialog">
    <template v-slot:activator="{ on }">
      <v-btn v-on="on">
        <span class="subtitle-1 white--text">Credits</span>
        <v-icon class="white--text">mdi-information-outline</v-icon>
      </v-btn>
    </template>
    <v-row justify="center">
      <v-card max-width="500px">
        <v-card-title class="headline">Credits</v-card-title>
        <v-card-text
          class="subtitle-1"
        >Les éléments contenus dans le présent site Internet, en particulier les images, les musiques, les logos, les éléments graphiques, sont la propriété de Philippe Fournier (fourniervoquer@gmail.com). Ils constituent des œuvres protégées par le droit d'auteur, en particulier par les dispositions du Code de la Propriété intellectuelle français et des traités internationaux régulièrement ratifiés par la France. Toute reproduction partielle ou totale à usage collectif est strictement interdite sans autorisation.</v-card-text>
        <v-card-title class="headline">Remerciements</v-card-title>
        <v-card-text class="subtitle-1">Merci à Ewen Bouquet pour la conception du site !</v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="green darken-1" text @click="dialog = false">Agree</v-btn>
        </v-card-actions>
      </v-card>
    </v-row>
  </v-dialog>
</template>

<script>
export default {
  name: "Law",
  data() {
    return {
      dialog: false
    };
  }
};
</script>