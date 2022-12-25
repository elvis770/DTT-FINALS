<template>
  <div class="delete">
      <div class="container">
        <listing/> 
      </div>

      <div class="popup">

          <h3> Delete Listing</h3>

          <h5> Are you sure you want to delete this listing?
               <br>
                     This action cannot be undone </h5>

            <div class="btns">

                <button class="btn--one"> Yes, Delete</button> <br>

                <router-link to="/listing">
                <button class="btn--two"> Go Back</button></router-link>
            </div>
         
      </div>
  </div>

  
</template>

<script>
// @ is an alias to /src


import Listing from '@/views/ListingView.vue'

export default {
  name: 'DeleteView',
  components: {
  
    Listing
    
    
  }
}
</script>

<style scoped>
.container{
    position: relative;
    box-shadow: 0 3px 10px rgb(0, 0, 0, 0.2);
    
}
.popup{
    position: fixed;
    top: 50%;
    left: 30%;
    right: 30%;
    z-index: 99;
    font-family: 'montserrat', sans-serif;
    
    
    background-color: #ffffff;
    width: 500px;
    height: auto;

    border-radius: 5px;
}
h3{
    font-family: 'montserrat', sans-serif;
    font-size: 18px;
    padding-left: 40%;
    padding-bottom: 20px;
}
h5{
    font-family: 'montserrat', sans-serif;
    font-size: 12px;
    color: #4A4B4C;
    padding-left: 28%;
    padding-bottom: 20px;
}
.btns{
    padding-left: 23%;
}
.btn--one{
    background-color: #EB5440;
    color: #FFFFFF;
   width: 300px;
    min-height: 35px;
    font-size: 14px;
    border: none;
    border-radius: 10px;

   
   
}
.btn--two{
    margin-top: 10px;
    margin-bottom: 10px;
    background-color: #4A4B4C;
    color: #FFFFFF;
   width: 300px;
    min-height: 35px;
    font-size: 14px;
    border: none;
    border-radius: 10px;
}

@media screen and (max-width: 40em) 
{
  .popup{
      top: 30%;
      left: 0;
      right: 0;
      bottom: 30%;

    width: 400px;
    height: 250px;

    border-radius: 5px;
    margin: 5px;
  }

  h3{
      padding-left: 30%;
      padding-bottom: 10px;
  }
  h5{
       padding-left: 18%;
  }
  .btns{
    padding-left: 22%;
}
.btn--one{
    width: 200px;
}
.btn--two{
    width: 200px;
}
}
</style>