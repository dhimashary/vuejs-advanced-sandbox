<template>
  <div class="col-8">
    <h2>User Address</h2>
    <p>{{ address }}</p>
  </div>
</template>

<script>
export default {
  name: 'UserStatus',
  props: ['address']
}
</script>
