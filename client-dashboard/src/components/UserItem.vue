<template>
  <tr>
    <th scope="row">{{i}}</th>
    <td>{{user.name}}</td>
    <td>{{user.username}}</td>
    <td>{{user.email}}</td>
    <td>{{user.address.city}}</td>
    <td>
      <button class="btn btn-primary btn-sm" @click="goDetail">
        See Detail
      </button>
    </td>
  </tr>
</template>

<script>
export default {
  name: 'UserItem',
  props: ['user', 'i'],
  methods: {
    goDetail () {
      // push ke path sesuai dengan user.id
    }
  }
}
</script>

<style>

</style>
