<template>
   <div class="card shadow card-product" style="width: 18rem;">
      <img :src=" '../assets/images/' + product.gambar " class="card-img-top">
        <div class="card-body">
            <h5 class="card-title">{{ product.nama }}</h5>
            <p class="card-price"> Harga : Rp. {{ product.harga }}</p>
            <a href="#" class="btn btn-primary"><b-icon-cart-plus-fill></b-icon-cart-plus-fill> Order</a>
        </div>
    </div>


</template>

<script>
export default {
    name: 'CardProduct',
    props:  ['product']
}
</script>

<style>

</style>