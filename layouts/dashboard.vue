<template>
  <div class="w-screen h-screen">
      <div class="w-full h-full flex">
          <div class="flex w-1/6 bg-red-500">
            <sidemenu>
                <template v-slot:sideMenuItems>
                    <!-- Home -->
                    <sidemenuitem path="/" pathName="Home">
                    <template v-slot:pathIcon>
                        <i class="fas fa-home"></i>
                    </template>
                    </sidemenuitem>
                    <!-- Product -->
                    <sidemenuitem path="/product" pathName="Product">
                    <template v-slot:pathIcon>
                        <i class="fas fa-seedling"></i>
                    </template>
                    </sidemenuitem>
                    <!-- Product New-->
                    <sidemenuitem path="/new" pathName="New">
                    <template v-slot:pathIcon>
                        <i class="fas fa-money-check-alt"></i>
                    </template>
                    </sidemenuitem>
                    <!-- Product Update-->
                    <sidemenuitem path="/update" pathName="Update">
                    <template v-slot:pathIcon>
                        <i class="fas fa-seedling"></i>
                    </template>
                    </sidemenuitem>
                    <!-- Product Inactive-->
                    <sidemenuitem path="/inactive" pathName="Inactive">
                    <template v-slot:pathIcon>
                        <i class="fas fa-seedling"></i>
                    </template>
                    </sidemenuitem>
                    
                </template>
            </sidemenu>
          </div>
          <div class="flex w-full bg-blue-500">
              <Nuxt />
          </div>
      </div>
  </div>
    

</template>

<script>
import sidemenu from '../components/sidemenu.vue'
export default {
  components: { sidemenu },

}
</script>

<style>

</style>