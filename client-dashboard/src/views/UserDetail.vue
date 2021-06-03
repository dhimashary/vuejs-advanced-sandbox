<template>
  <div class="container">
    <h1>User Detail {{ userDetail.name }}</h1>
    <div class="row">
      <div class="col-12">
        <button class="btn btn-primary me-3" @click="$router.push('address')">See Address</button>
        <button class="btn btn-success" @click="$router.push('status')">See Status</button>
      </div>
      <div class="col-4">
        <ul class="list-group">
          <li class="list-group-item">username: {{userDetail.username}}</li>
          <li class="list-group-item">email: {{userDetail.email}}</li>
        </ul>
      </div>
      <!-- letakkan router-view disini -->
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'UserDetail',
  data () {
    return {
      userDetail: {}
    }
  },
  methods: {
    fetchDetail () {
      axios({
        method: 'GET',
        url: `https://jsonplaceholder.typicode.com/users/${this.$route.params.id}`
      })
        .then(({ data }) => {
          this.userDetail = data
        })
        .catch(err => {
          console.log(err)
        })
    }
  },
  created () {
    this.fetchDetail()
  }
}
</script>

<style>

</style>
