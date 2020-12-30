<template>
 <!-- <Logos /> -->
 <div id="app">
   <div class="container">
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
             <div class="form-check">
              <input class="form-check-input" onclick="" type="checkbox" value="" v-bind:id="`todo-`+tugasSaya.id">
              <!-- setiap pengambilan data dari v-for gunakan v-bind: terus sesuaikan dengan javascript biasa (ini brarti id nya todo-id id dari si data jsonnya)-->
              <label class="form-check-label item" v-bind:for="`todo-`+tugasSaya.id">
                {{tugasSaya.namaTugas}}
              </label>
            </div>
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

export default {
  name: 'App',
  data:function(){
    return {
      tugas : [
        {
          id: 1,
          namaTugas: "Mengerjakan PR",

        },
        {
          id:2,
          namaTugas: "Menyapu Rumah"
        },
        {
          id:3,
          namaTugas: "Membersihkan Kasur"
        },
        {
          id:4,
          namaTugas: "Tidur"
        }
      ]
    }
  },
  components: {
    // Logos
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
</style>
