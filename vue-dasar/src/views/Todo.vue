<template>
 <!-- <Logos /> -->
 <div id="app">
   <div class="container abc">
     <div class="row header mb-5 p-3">
       <div class="col-lg-12">
         <h2>To Do List</h2>
       </div>
     </div>
     <div class="row content">
       <div class="col-lg-12">
         <div class="pekerjaan-rumah">
           <div class="row">
            <div class="tugas text-left mb-4 col-lg-12" v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id">
              <!-- v-for untuk looping data v bind:key untuk menentukan data berdasarkan apa -->
            
            <!-- pashing melempar data  -->
            <ItemTugas v-bind:tugasSaya="tugasSaya"/>
            <!-- melempar data ke ItemTugas.vue -->
          </div>
          </div>
        </div>
       </div>
     </div>
   </div>
   
   
 </div>
</template>

<script>
// import Logos from './components/Logos.vue'

//atau bisa taro di main.js library nya
import 'bootstrap/dist/css/bootstrap.css';
import ItemTugas from '@/components/ItemTugas.vue'

export default {
  name: 'Todo',
  data:function(){
    return {
      tugas : [
        {
          id: 1,
          namaTugas: "Mengerjakan PR",
          isDone:false
        },
        {
          id:2,
          namaTugas: "Menyapu Rumah",
          isDone:false
        },
        {
          id:3,
          namaTugas: "Membersihkan Kasur",
          isDone:false
        },
        {
          id:4,
          namaTugas: "Tidur",
          isDone:false
        }
      ]
    }
  },
  components: {
    // Logos
    ItemTugas
  }
}


</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.header{
  background: #1abc9c;
}

.header h2 {
  margin: 0;
  color:white
}

.tugas .item {
  font-size:20px
}

.item-completed {
color: #1abc9c;
}
</style>