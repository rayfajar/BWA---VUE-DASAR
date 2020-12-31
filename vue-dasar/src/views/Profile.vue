<template>
  <div class="profile">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-8">
          <div class="media text-left">
            <img class="mr-3 user-pic"  src="../assets/profile.jpg">
            <div class="media-body">
              <h5 class="mt-0">{{ firstName }} {{ lastName }}</h5>
              <p> {{ aboutMe }}.</p>
             
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import dependecies / import css bootstrap
// import 'bootstrap/dist/css/bootstrap.css'

export default {
  name: 'Profile',
  data : function(){
    return {
  // property: value
    firstName: "Ray",
    lastName : "Fajar",
    aboutMe : "A passionate Web Front-end Developer from Indonesia"
    }
    
  },
  components: {
  }
}
</script>

<style scoped>
  .user-pic{
    height: 200px;
    width: 200px;
    border-radius: 200%;
  }

</style>