<template>
  <v-container full-height class="py-0">
    <v-row>
      <v-col cols="12">
        <card-list v-model="items" #default="{ item }">
          <v-row>
            <v-col cols="12">
              <v-text-field v-model="item.name" label="Name" hide-details />
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="12">
              <v-text-field v-model="item.email" label="Email" hide-details />
            </v-col>
          </v-row>
        </card-list>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="auto" class="py-0 mx-auto">
        <v-btn @click="add" text>
          <v-icon>
            mdi-plus
          </v-icon>
          Add
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import CardList from '@/components/CardList'

export default {
  components: {
    CardList
  },

  data: () => ({
    items: [],

    counter: 0
  }),

  methods: {
    add () {
      this.items.push({ id: this.counter++ })
    }
  }
}
</script>
