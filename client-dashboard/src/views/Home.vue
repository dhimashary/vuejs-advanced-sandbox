<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <UserList :users="users"/>
  </div>
</template>

<script>
import UserList from '@/components/UserList.vue'
import axios from 'axios'

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
      axios({
        method: 'GET',
        url: 'https://jsonplaceholder.typicode.com/users'
      })
        .then(({ data }) => {
          this.users = data
        })
        .catch(err => {
          console.log(err)
        })
    }
  },
  created () {
    this.fetchUsers()
  }
}
</script>
