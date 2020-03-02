<template>
  <v-container full-height>
    <v-row>
      <v-col cols="6" offset="3">
        <card-list v-model="items" #default="{ item }">
          <v-row>
            <v-col cols="12">
              <v-text-field v-model="item.name" label="Name" type="string" />
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="12">
              <v-text-field v-model="item.email" label="Email" type="string" />
            </v-col>
          </v-row>
        </card-list>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import CardList from '@/components/CardList'

export default {
  components: {
    CardList
  }

  data: () => ({
    items: []
  })
}
</script>
