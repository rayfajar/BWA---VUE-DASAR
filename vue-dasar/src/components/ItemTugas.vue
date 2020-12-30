<template>
<div>
<!-- <div class="form-check"> -->
              <input class="form-check-input" onclick="" type="checkbox" value="" v-bind:id="`todo-`+tugasSaya.id">
              <!-- setiap pengambilan data dari v-for gunakan v-bind: terus sesuaikan dengan javascript biasa (ini brarti id nya todo-id id dari si data jsonnya)-->
              <label class="form-check-label item" v-bind:class="{'item-completed':tugasSaya.isDone}" v-bind:for="`todo-`+tugasSaya.id">
                <!-- conditional rendering vue js, untuk membuat 1 statment pada interface, ini kalo true warna bakalan berubah jadi yg gak beres
                gakan nambahin class nya
                 -->
                {{tugasSaya.namaTugas}}
              </label>
     <!-- </div> -->
</div>
</template>


<script>
export default {
    name: "ItemTugas",
    props:["tugasSaya"]
    // ngambil data dari app.vue biar bisa di printing out di tugas saya
}
</script>



<style lang="stylus" scoped>

</style>