<template>
  <div class="food">
       <Navbar />
       <div class="container">
          <div class="row mt-4">
            <div class="col">
              <h2><strong>Foods</strong> List</h2>
            </div>
          </div>
          <div class="row mt-5">
            <div class="col">
              <div class="input-group mb-3">
                <input type="text" class="form-control" v-model="search" @keyup="searchFoods" placeholder="Search your foods favorite" >
                <div class="input-group-append">
                  <span class="input-group-text" id="basic-addon2"><b-icon-search></b-icon-search></span>
                </div>
              </div>
            </div>
            
          </div>
          
           <div class="row mb-4">
              <div class="col md-4 mt-4 ml-auto" v-for="product in products" :key="product.id">
                <CardProduct :product="product"/>
              </div>
           </div>
          
       </div>
     
  </div>
 
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import CardProduct from '@/components/CardProduct.vue'
import axios from "axios"

export default {
  name: 'Food',
  components: {
    Navbar,
    CardProduct
  },
  data() {
    return{
      products: [],
      search: ''
    }
  },
  methods: {
      setProduct(data) {
          this.products = data;
      },
      searchFoods() {
         axios.get('http://localhost:3000/products?q='+this.search)
        .then((response) => this.setProduct(response.data))
        .catch((error) => console.log(error))
      }
  },
  mounted() {
      axios.get('http://localhost:3000/products')
      .then((response) => this.setProduct(response.data))
      .catch((error) => console.log(error))
     
  }
}
</script>

<style>

</style>