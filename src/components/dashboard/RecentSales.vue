<template>
  <v-card
    class="mx-auto text-center"
    dark
    min-height="400" 
    max-width="600"
  >
    <v-card-text>
      <v-sheet color="rgba(33, 32, 28, .4)">
        <v-sparkline
          :value="value"
          color="#DFE0E2"
          height="100"
          padding="14"
          stroke-linecap="round"
          smooth
        >
          <template v-slot:label="item">
            ${{ item.value }}
          </template>
        </v-sparkline>
      </v-sheet>
    </v-card-text>

    <v-card-text>
      <div class="display-1 font-weight-thin">
        Sales Last 24h
      </div>
    </v-card-text>

    <v-divider></v-divider>

    <v-card-actions class="justify-center">
      <v-btn
        block
        text
      >
        Go to Report
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      value: [
        423,
        446,
        675,
        510,
        590,
        610,
        760,
      ],
    }),
  }
</script>