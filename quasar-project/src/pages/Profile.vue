<template>
  <q-page padding>
    <!-- content -->
    <h3>Profile</h3>
  </q-page>
</template>

<script>
export default {
  async created() {
    const character = this.$axios.get(`https://www.breakingbadapi.com/api/characters/${this.$route.params.id}`)
    console.log(character.data);
  },
  data: function() {
    return {
      character: '',
    }
  }
}
</script>
