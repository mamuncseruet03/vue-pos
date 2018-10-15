<template>
  <div>
    <div>
      <form>
        <div v-if="showLogIn">
          Please Log in
        </div>
        <div>
          <input type="email" v-model="email" class="email" name="email" placeholder="Enter eamil" required>
        </div>
        <div>
          <input type="password" v-model="password" class="password" name="password" placeholder="Enter password" required>
        </div>
        <div>
          <!-- <button type="submit">Login</button> -->
          <md-button type="button" class="md-primary" @click="submitLogin">Log In</md-button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
import Vue from 'vue'
import VueMaterial from 'vue-material'
import axios from 'axios'
import 'vue-material/dist/vue-material.min.css'
// import {BrowserWindow} from 'electron'

Vue.use(VueMaterial)

export default {
  props: [
    'isLoggedIn'
  ],
  data () {
    return {
      email: '',
      password: '',
      showLogIn: true
    }
  },
  mounted () {
    this.showLogIn = !this.isLoggedIn
  },
  methods: {
    submitLogin () {
      console.log('login clicked', this.email, this.password)
      this.showLogIn = !this.showLogIn
      // let win = new BrowserWindow({show: false})
      // win.loadUrl('http://www.google.com')
      // win.show()
      // axios.post('http://www.google.com', {
      //   email: this.email,
      //   password: this.password
      // })
      //   .then((res) => {
      //     console.log('login pressed')
      //   // this.isLogin = true;
      //   })
      //   .catch((error) => console.log(error))
    },
    ajaira () {
      axios.get('http://www.google.com')
    }
  }
}
</script>
<style>
  .email, .password {
    margin: 10px 10px 10px 0;
    padding: 5px;
  }
</style>
