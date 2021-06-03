<template>
  <table class="table">
    <thead>
      <tr>
        <th scope="col">No</th>
        <th scope="col">Name</th>
        <th scope="col">Username</th>
        <th scope="col">Email</th>
        <th scope="col">City</th>
        <th scope="col">Action</th>
      </tr>
    </thead>
    <tbody>
      <UserItem v-for="(user, i) in users" :key="user.id" :user="user" :i="i+1"/>
    </tbody>
  </table>
</template>

<script>
import UserItem from './UserItem'

export default {
  name: 'UserList',
  components: {
    UserItem
  },
  computed: {
    users () {
      return this.$store.state.users
    }
  }
}
</script>

<style>
</style>
