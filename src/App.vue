<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <div class="col-6">
          <v-jsoneditor v-model="json"
                        @input="jsonChanged">
          </v-jsoneditor>
        </div>

        <div class="col-6">
          <MobilePhone v-bind:json="json">
          </MobilePhone>
        </div>

      </div>
    </div>

  </div>
</template>

<script>
import 'bootstrap'
import 'bootstrap/dist/css/bootstrap.min.css'
import VJsoneditor from 'vue-jsoneditor'
// import HelloWorld from './components/HelloWorld.vue'
import MobilePhone from './components/MobilePhone.vue'

export default {
  name: 'app',
  components: {
    // HelloWorld,
    VJsoneditor,
    MobilePhone
  },
  data() {
    return {
      json: {
        sucess: true,
        title: 'Title',
        description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
      },
    };
  },
  methods: {
    jsonChanged(value) {
      console.log(JSON.stringify(value));
    },
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.jsoneditor {
  background: white;
}
</style>
