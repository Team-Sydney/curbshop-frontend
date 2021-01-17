<template>
  <v-app-bar
    absolute
    app
    color='white'
    elevation=0
  >
    <v-toolbar-title
      class="businessName hidden-sm-and-down"
    >
      Donut Monster
    </v-toolbar-title>

    <v-spacer/>

    <v-btn icon>
      <v-icon>mdi-account</v-icon>
    </v-btn>
  </v-app-bar>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600;700&display=swap');


.businessName {
  font-family: 'Quicksand', sans-serif;
  font-weight: 700;
  font-size: 1.9em;
}

</style>