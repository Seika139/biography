<template>
  <v-app-bar
    app
    color="indigo"
    dark>
    <h2 class="headline font-weight-bold">
      Portfolio site
    </h2>

    <v-spacer></v-spacer>

    <v-col cols="6" sm="3" lg="2">
      <v-select
      v-model="selectedId"
      :items="languages"
      item-text="text"
      item-value="id"
      label="Language"
      class="mt-8"
      height="100"
      @change="change()"
      ></v-select>
    </v-col>

  </v-app-bar>

</template>

<script>

  export default {
    name: 'Navigation',

    props: {
      languageId: {
        type: Number,
        default: 0,
      }
    },

    data() {
      return {
      selectedId: this.languageId
      }
    },

    computed: {
      languages() {
        return [
          { id: 0, text: '日本語' },
          { id: 1, text: 'English' }
        ]
      }
    },

    methods: {
      change() {
        this.$emit('change', this.selectedId)
      },
    }
  }

</script>