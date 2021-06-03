<template>
  <div class="about">
    <h1>This is Dashboard Page</h1>
    <VisitorCount />
  </div>
</template>

<script>
import VisitorCount from '../components/VisitorCount'
export default {
  name: 'Dashboard',
  components: {
    VisitorCount
  }
}
</script>
