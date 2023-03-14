<template>
    <div class="">
      <NavBar />
      <h2>Our Products</h2>
      <div class="container">
        <div class="row">
            <div class="col-md-3" v-for="product in products" :key="product.id">
                <div class="card mt-2">
                <img :src="product.thumbnail" alt="" height="150">
                  <div class="card-body">
                      <strong>{{ product.title.substring(0,10) }}</strong>
                      <strong>{{ product.price }}</strong>
                      <p>{{ product.description.substring(0, 50)  }} </p>
                      <button class="btn btn-primary">Add to cart</button>
                  </div>
                </div>
            </div>
        </div>
      </div>
      
    </div>
  </template>
    
    <script>
  import NavBar from "../components/NavBar.vue";
  import axios from "axios";
   
  export default {
    // name: 'ProductView',
    components: {
      NavBar,
    },
  
    data() {
      return {
        products: null,
      };
    },
    mounted() {
      axios.get("https://dummyjson.com/products")
        .then((response) => {
            this.products = response.data.products
            console.log(response.data.products)
           
        })
  
        .catch((error) => {
          console.log(error)
        })
    },
  };
  </script>
    