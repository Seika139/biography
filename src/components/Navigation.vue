<template>
  <v-app-bar
    app
    color="indigo"
    dark>
    <v-app-bar-nav-icon></v-app-bar-nav-icon>

    <v-spacer></v-spacer>

    <v-col cols="2">
      <v-select
      v-model="selectedId"
      :items="languages"
      item-text="text"
      item-value="id"
      label="Language"
      class="mt-7"
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
          { id: 0, text: 'Japanese' },
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