<script>
const API_URL = `http://127.0.0.1:8000/hello/oui/cyprien`;

export default {
  data: () => ({
    message: null
  }),

  created() {
    this.fetchData();
  },

  methods: {
    async fetchData() {
      this.message = await (await fetch(API_URL)).json();
    }
  }
}
</script>

<template>
  <div>
    <h1>Message from API</h1>
    <p>{{ message }}</p>
  </div>
</template>

<style>
/* ajoutez vos styles ici */
</style>
