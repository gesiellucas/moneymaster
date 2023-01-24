<template>
    <div>
      <form @submit.prevent="login">
        <label for="username">Username</label>
        <input v-model="username" id="username" type="text"/>
        <label for="password">Password</label>
        <input v-model="password" id="password" type="password"/>
        <button>Login</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        username: '',
        password: ''
      }
    },
    methods: {
      login() {
        // Make a request to the server to check the provided credentials
        // and handle the response accordingly
        // 
        // Example:
        // axios.post('/login', {username: this.username, password: this.password})
        // .then(response => {
        //  if(response.data.success) {
        //    // handle successful login
        //  } else {
        //    // handle failed login
        //  }
        // })
        // .catch(error => {
        //  // handle error
        // });
        console.log('ok')
      }
    }
  }
  </script>
  