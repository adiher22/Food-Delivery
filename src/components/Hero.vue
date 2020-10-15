<template>
   <div class="hero">
       <!-- Desktop Version -->
    <div class="d-md-block d-none">
      <div class="row mt-4">
        <div class="col-md-6">
          <div class="d-flex h-100">
              <div class="justify-content-center align-self-center">
                  <h2><strong>Delicious Food Menu </strong><br> in Your Gadget</h2>
                  <p>Choose and order your favorite foods</p>
                  <router-link class="btn btn-primary btn-lg" to="/food">
                      <b-icon-arrow-right></b-icon-arrow-right> Order Now
                  </router-link>
              </div>
              
          </div>
          
      </div>
      <div class="col-md-6">
          <img src="../assets/images/foods.svg" class="w-100" alt="">
      </div>
    </div>
    </div>
    <div class="d-sm-block d-md-none">
      <!-- Mobile Version -->
     <div class="row mt-4">
         <div class="col-md-6 mb-4">
                <img src="../assets/images/foods.svg" class="w-100" alt="">
         </div>
        <div class="col-md-6">
            <div class="d-flex h-100">
                <div class="justify-content-center align-self-center">
                    <h2><strong>Delicious Food Menu </strong><br> in Your Gadget</h2>
                    <p>Choose and order your favorite foods</p>
                    <button class="btn btn-primary btn-lg"><b-icon-arrow-right></b-icon-arrow-right> Order Now</button>
                </div>
                
            </div>
            
        </div>
      
    </div>
   </div>
  </div>
   
</template>

<script>
export default {
    name: 'Hero'
}
</script>

<style>

</style>