<template>
  <v-app>
   <Navbar />
   <Todos />
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';
import Navbar from './components/Navbar.vue';
import Todos from './components/Todos.vue';

export default Vue.extend({
  name: 'App',
  components: {
    Navbar,
    Todos,
  },
  data: () => ({
    //
  }),
});
</script>
