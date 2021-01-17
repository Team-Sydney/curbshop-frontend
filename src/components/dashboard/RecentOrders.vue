<template>
  <v-card dark min-height="400px" min-width="650" max-width="700">
    <v-list-item>
      <v-list-item-content>
        <v-list-item-title class="headline">Recent Orders</v-list-item-title>
      </v-list-item-content>
    </v-list-item>

    <v-data-table
      hide-default-footer 
      :headers="headers"
      :items="orders"
    >
    </v-data-table>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      headers: [
        { text: 'Product Name', align: 'start', value: 'name' },
        { text: 'Status', align: 'start', value: ''}
        { text: 'Quantity', align: 'start', value: 'quantity' },
        { text: 'Total Price', align: 'start', value: 'totalPrice' },
        { text: 'Date', align: 'start', value: 'orderDate' }
      ],
      orders: [
        {
          name: 'Sprinkle Shit',
          quantity: 10,
          totalPrice: '$30.10',
          orderDate: '1/17/2021'
        },
        {
          name: 'Jacket',
          quantity: 1,
          totalPrice: '$84.50',
          orderDate: '1/17/2021'
        },
        {
          name: 'Socks',
          quantity: 2,
          totalPrice: '$20.34',
          orderDate: '1/17/2021'
        },
        {
          name: 'Water Bottle',
          quantity: 1,
          totalPrice: '$15.15',
          orderDate: '1/17/2021'
        },
        {
          name: 'Stuffed Animal Owl',
          quantity: 1,
          totalPrice: '$54.12',
          orderDate: '1/17/2021'
        }
      ]
    }
  }
}
</script>

<style scoped>
.v-data-table td {
    border-bottom: none !important;
}
</style>