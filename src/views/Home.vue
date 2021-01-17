<template>
  <v-row>
    <v-col cols="12" md="6">
      <RecentOrders/>
    </v-col>
    <v-col cols="12" md="6">
      <RecentSales/>
    </v-col>
  </v-row>
</template>

<script>
// @ is an alias to /src
import Sidebar from '@/components/Sidebar.vue'

import RecentOrders from '@/components/dashboard/RecentOrders.vue'
import RecentSales from '@/components/dashboard/RecentSales.vue'

export default {
  name: 'Home',
  components: {
    Sidebar,
    RecentOrders,
    RecentSales
  }
}
</script>

