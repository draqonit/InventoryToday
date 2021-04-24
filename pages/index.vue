<template>
  <div class="w-screen h-screen bg-yellow-500 p-20">
      <div class="text-blue-700 text-2xl">
      PARENT <i class="fas fa-igloo"></i>
      </div>
      <div class="flex w-1/2 bg-red-500 p-14 md:bg-blue-500">
          CHILD <i class="fab fa-cpanel"></i>
          
      </div>
      <div class="flex w-1/2 bg-blue-500 p-14 md:bg-red-500">
          CHILD 2 {{products}}
          <testimonial
              img_src="https://images.unsplash.com/photo-1499714608240-22fc6ad53fb2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80"
              name="afza"
              title="Hello"
              content="lorem"
              >
          </testimonial>
      </div>
      
  </div>
</template>

<script>
import { mapActions, mapState} from 'vuex';
export default {
    computed: {
        ...mapState({
            products: state => state.product.products
        })
    },

    methods: {
        ...mapActions({
            getProducts: "product/getProducts"
        })
    },

    mounted(){
        this.getProducts();
    }
}

</script>
