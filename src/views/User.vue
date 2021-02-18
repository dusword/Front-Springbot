<template>
  <div>
    <table>
      <tr>
        <th>Id</th>
        <th>Name</th>
        <th>Password</th>
      </tr>
      <tr v-for="user in users">
        <td>{{ user.user_ID }}</td>
        <td>{{ user.user_NAME }}</td>
        <td>{{ user.user_PASSWORD }}</td>
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
          user_ID: 1,
          user_NAME: 'lxj1',
          user_PASSWORD: '123456'
        },
        {
          user_ID: 1,
          user_NAME: 'lxj1',
          user_PASSWORD: '123456'
        },        {
          user_ID: 1,
          user_NAME: 'lxj1',
          user_PASSWORD: '123456'
        }
      ]
    }
  },
  created() {
    const _this=this
    axios.get("http://localhost:8081/user/findAll").then(function (response){
      console.log(response)
      _this.users=response.data
    })
  }
}
</script>

<style scoped>

</style>
