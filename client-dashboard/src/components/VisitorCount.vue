<template>
  <div>
    <h1>Visitor Count: {{ count }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Visitor Count',
  computed: {
    count () {
      // ambil count dari vuex state, ubah angka 0 dibawah ini
      return 0
    }
  }
}
</script>

<style>

</style>
