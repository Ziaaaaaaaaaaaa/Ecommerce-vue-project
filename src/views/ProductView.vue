<template>
  <div>
      <div class="container">
          <div class="row">
              <div class="col" v-for="item in productsData" :key="item.id">
                  <div class="card h-100" style="width: 18rem;">
                      <img :src="item.img" class="card-img-top" alt="...">
                      <div class="card-body">
                        <p class="card-text">{{ item.make }}</p>
                        <p class="card-text">{{ item.specs }}</p>
                        <p class="card-text">{{ item.Amount }}</p>
                        <router-link :to="{ name: 'test', params:{id: item.id }, query: {name: item.make, specs: item.specs, img: item.img}}"><button>go</button></router-link>
                      </div>
                    </div>
              </div>
          </div>
      </div>
  </div>
</template>

<script>
  export default {
    name: "App",
     computed:{
      productsData(){
        return this.$store.state.productsData
      }
     },
     methods:{
      getProduct(){
        this.$router.push({
          name: "test",
          params: {id: 1},
          query: {name: "test"}
        })
      }
     },
     mounted(){
      this.$store.dispatch('fetchData')
     }
  }
</script>

<style scoped>

</style>