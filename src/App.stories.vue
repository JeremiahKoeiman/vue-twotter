<template>
  <div id="apps">
    @{{ user.username }} - {{ fullName }}
    <strong>Followers: </strong> {{ followers }}
    <button @click="followUser">
      Follow
    </button>
  </div>
</template>

<script>
  export default {
    name: 'App',
    data () {
      return {
        followers: 0,
        user: {
          id: 1,
          username: 'Jerry',
          firstname: 'Jerry',
          lastname: 'Boy',
          email: 'jerryboy@gmail.com',
          isAdmin: true
        }
      }
    },
    computed: {
      fullName: function () {
        return `${this.user.firstname} ${this.user.lastname}`
      }
    },
    methods: {
      followUser() {
        this.followers++
      }
    }
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  display: flex;
  flex-direction: column;
  text-align: center;
}
</style>
