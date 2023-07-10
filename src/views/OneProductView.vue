<template>
    <div>
        <div class="container">
            <div class="row">
                <div class="col">
                    <div class="card h-100" style="width: 18rem;">
                        <img :src="$route.query.img" class="card-img-top" alt="...">
                        <div class="card-body">
                          <p class="card-text">{{ $route.query.name }}</p>
                          <p class="card-text">{{ $route.query.specs }}</p>
                        </div>
                      </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>

</style>