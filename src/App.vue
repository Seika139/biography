<template>
  <v-app>
    <navigation/>
    <v-content>
      <Body/>
    </v-content>
  </v-app>
</template>

<script>
import Body from './components/Body';
import Navigation from './components/Navigation';

export default {
  name: 'App',

  components: {
    Body,
    Navigation,
  },

  data: () => ({
    //
  }),
};
</script>
