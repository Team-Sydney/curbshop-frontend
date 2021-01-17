<template>
  <v-navigation-drawer app permanent>
    <v-list-item >
      <v-list-item-content>
        <v-list-item-title class="bigname">
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
        class="item"
        v-for="item in items"
        :key='item.title'
        :to='item.route'
      >
        <v-list-item-icon>
          <v-icon color='white'>{{ item.icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title class="white--text sidebar-item">{{ item.title }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>


    <template v-slot:append>
      <v-divider/>
      <div class="pa-2">
        <v-btn color="black" class="white--text" block>
          Business Profile
        </v-btn>
      </div>
      <div class="pa-2">
        <v-btn color="black" class="white--text" block>
          Logout
        </v-btn>
      </div>
    </template>

  </v-navigation-drawer>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: 'Dashboard', icon: 'mdi-view-dashboard', route: '/'},
        { title: 'Products', icon: 'mdi-dots-grid', route: '/products'},
        { title: 'Orders', icon: 'mdi-basket', route: '/orders'},
        { title: 'Sales', icon: 'mdi-point-of-sale', route: '/sales'}
      ]
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600;700&display=swap');

.item {
  background-color: black;
  color: white;
}

.bigname {
  font-family: 'Quicksand', sans-serif;
  font-size: 1.8em;
}

#name {
  font-weight: 700;
}

</style>