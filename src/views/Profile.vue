<template>
  <div class="profile">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <h1>This is a Profile page</h1>
    <br>
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-6">
          <div class="media text-left">
            <img class="user-pic mr-3" src="../assets/febryan.png" alt="Generic placeholder image">
            <div class="media-body">
              <h5 class="mt-0">{{namaDepan}} {{namaBelakang}}</h5>
              <p>{{deskripsi}}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import 'bootstrap/dist/css/bootstrap.css'

export default {
  name: 'Profile',
  data: function(){
    return{
      namaDepan: 'Febryan',
      namaBelakang: 'Ramadhan',
      deskripsi: 'Ini adalah deskripsi. Cras sit amet nibh libero, in gravida nulla. Nulla vel metus scelerisque ante sollicitudin. Cras purus odio, vestibulum in vulputate at, tempus viverra turpis. Fusce condimentum nunc ac nisi vulputate fringilla. Donec lacinia congue felis in faucibus.'
    }
  },
  components: {
    // HelloWorld
  }
}
</script>

<style scoped>
    .user-pic{
      border-radius: 200%;
      width: 100px;
      height: 100px;
    }
</style>