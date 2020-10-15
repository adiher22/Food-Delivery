<template>
<nav class="navbar navbar-expand-lg navbar-light">
    <div class="container">    
        <router-link class="navbar-brand" to="/">Food Delivery</router-link>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavDropdown">
            <ul class="navbar-nav mr-auto">
            <li class="nav-item">
                <router-link class="nav-link" to="/">Home</router-link>
            </li>
            <li class="nav-item">
                <router-link class="nav-link" to="/food">Food</router-link>
            </li>
            <li class="nav-item">
                <router-link class="nav-link" to="/categories">Categories</router-link>
            </li>
            
            </ul>
            <ul class="navbar-nav ml-auto">
            <li class="nav-item">
                <router-link class="nav-link" to="/cart">Cart
                <b-icon-bag-dash>
                </b-icon-bag-dash>
                <span class="badge badge-primary ml-2">3</span>
                </router-link>
            </li>
            
            
            </ul>
        </div>
    </div>
</nav>
</template>

<script>
export default {
    name: 'Navbar'
}
</script>

<style>

</style>