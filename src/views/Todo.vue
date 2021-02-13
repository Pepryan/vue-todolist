<template>
  <div class="todo">
    <div class="container">
      
      <div class="row header mb-3 p-3">
        <div class="col-lg-12">
          <h1>This is my To-do list</h1>
          <h3>What I do today?</h3>
          <hr>
        </div>
      </div>

      <div class="row content">
        <div class="col-lg-12">
          <div class="todo-list">
            <div class="row justify-content-center">
              <div class="col-lg-2 text-left">
                <h5>Task</h5>
              </div>
              <div class="col-lg-2 text-left">
                <h5>Category</h5>
              </div>


            </div>
            <div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id">  
              <ItemTodo v-bind:tugasSaya="tugasSaya"/>
            </div>
          </div>
        </div>
      </div>

    </div> <!-- .container -->
  </div> <!-- .todo -->
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import 'bootstrap/dist/css/bootstrap.css';
import ItemTodo from '../components/ItemTodo.vue';

export default {
  name: 'Todo',
  data: function(){
    return{
      tugas: [
        {
          id: 1,
          namaTugas: 'Cleaning my room ',
          kategori: 'Personal',
          isDone: false
        },
        {
          id: 2,
          namaTugas: 'Coding website',
          kategori: 'Work',
          isDone: false
        },
        {
          id: 3,
          namaTugas: 'Gym',
          kategori: 'Sport',
          isDone: false
        },
        {
          id: 4,
          namaTugas: 'Drink milk',
          kategori: 'Personal',
          isDone: false
        }
      ]
    }
  },
  components: {
    // HelloWorld
    ItemTodo
  },
  methods:{
    toogleTugas: function(tugasSaya){
      tugasSaya.isDone = !tugasSaya.isDone;
    
    }
  }
}
</script>

<style scoped>
    .user-pic{
      border-radius: 200%;
      width: 100px;
      height: 100px;
    }
    /* .header{
      background: blueviolet;
    } */
    .header h3{
      margin: 0;
    }
    .item-tugas-selesai{
      text-decoration: line-through;
    }
</style>