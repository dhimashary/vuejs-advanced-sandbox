<template>
  <div class="about">
    <h1>This is Dashboard Page</h1>
    <p>
      Tambahkan beforeRouteEnter yang akan mengecek apakah user memiliki access_token / tidak di localStorage pada Views "Dashboard", jika user tidak memiliki access_token alihkan ke halaman login
    </p>
  </div>
</template>

<script>
export default {
  name: 'Dashboard'
}
</script>
