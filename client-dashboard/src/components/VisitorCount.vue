<template>
  <div>
    <h1>Visitor Count: {{ count }}</h1>
    <AddCount />
  </div>
</template>

<script>
import AddCount from './AddCount'

export default {
  name: 'Visitor Count',
  computed: {
    count () {
      return this.$store.state.count
    }
  },
  components: {
    AddCount
  }
}
</script>

<style>

</style>
