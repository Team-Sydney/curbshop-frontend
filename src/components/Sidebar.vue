<template>
  <v-navigation-drawer app permanent>
    <v-list-item>
      <v-list-item-content>
        <v-list-item-title class="title">
          <span id="name">curbshop</span>.online
        </v-list-item-title>
      </v-list-item-content>
    </v-list-item>

    <v-divider/>

    <v-list
      dense
      nav
    >
      <v-list-item
        v-for="item in items"
        :key='item.title'
        :to='item.route'
      >
        <v-list-item-icon>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600;700&display=swap');

.title {
  font-family: 'Quicksand', sans-serif;
  font-size: 2.2em;
}

#name {
  font-weight: 700;
}

</style>