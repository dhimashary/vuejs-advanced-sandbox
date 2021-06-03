<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <UserList />
  </div>
</template>

<script>
import UserList from '@/components/UserList.vue'

export default {
  name: 'Home',
  data () {
    return {
      users: []
    }
  },
  components: {
    UserList
  },
  methods: {
    fetchUsers () {
      // pindahkan method ini ke action
    }
  },
  created () {
    // panggil action fetchUser disini
  }
}
</script>
