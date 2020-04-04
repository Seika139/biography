<template>
  <v-col class="mb-5" cols="12">
    <h2 class="headline font-weight-bold mb-3">
      <v-icon dence>mdi-school</v-icon>
      History
    </h2>

    <v-timeline dense>
      <v-timeline-item v-for="(item,i) in timelineItems" :key="i">
        <v-card class="elevation-2">
          <v-card-title class="headline">{{ item.title }}</v-card-title>
          <v-card-text>
            {{ item.text }}
          </v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </v-col>
</template>

<script>
export default {
  name: 'History',

  computed: {
    timelineItems() {
      return [
        { title: "First", text: "English", date: "2015"},
        { title: "First", text: "English", date: "2015"},
        { title: "First", text: "English", date: "2015"},
      ]
    }
  }
}
</script>