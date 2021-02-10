<template>
  <div>
    <table>
      <tr>
        <th>Id</th>
        <th>Name</th>
        <th>Password</th>
      </tr>
      <tr v-for="user in users">
        <td>{{ user.id }}</td>
        <td>{{ user.name }}</td>
        <td>{{ user.password }}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: "User",
  data() {
    return {
      users: [
        {
          id: 1,
          name: 'lxj1',
          password: '123456'
        },
        {
          id: 2,
          name: 'lxj2',
          password: '123456'
        },
        {
          id: 3,
          name: 'lxj3',
          password: '123456'
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>
