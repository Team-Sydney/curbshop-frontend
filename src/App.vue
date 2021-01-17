<template>
  <v-app dark>
    <Appbar/>
    <Sidebar/>
    <v-main>
      <v-container fluid>
        <router-view/>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Appbar from './components/Appbar';
import Sidebar from './components/Sidebar';

export default {
  name: 'App',

  components: {
    Sidebar,
    Appbar
  },

  data: () => ({
    //
  }),
};
</script>
