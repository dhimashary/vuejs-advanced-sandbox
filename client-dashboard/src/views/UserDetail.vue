<template>
  <div>
    <h1>Ini halaman User Detail</h1>
    <div>
      {{ userDetail }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'UserDetail',
  data() {
    return {
      userDetail: {}
    }
  },
  methods: {
    fetchDetail() {
      // fetch user detail sesuai dengan params id disini
    }
  },
  created() {
    // panggil method fetchdetail disini
  }
}
</script>

<style>

</style>