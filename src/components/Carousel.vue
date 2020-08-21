<template>
<div>
    <div id="carouselExampleInterval" class="carousel slide" data-ride="carousel">
        <div class="carousel-inner">
            <div class="carousel-item active" data-interval="10000">
                <img :src="a[0]">
            </div>
            <div class="carousel-item" data-interval="2000">
                <img :src="a[1]">
            </div>
            <div class="carousel-item">
                <img :src="a[2]">
            </div>
        </div>
        <a class="carousel-control-prev" href="#carouselExampleInterval" role="button" data-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="sr-only">Previous</span>
        </a>
        <a class="carousel-control-next" href="#carouselExampleInterval" role="button" data-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="sr-only">Next</span>
        </a>
    </div>
</div>
</template>

<script>
export default {
    data: function () {
        return {
            a:[
                require('../assets/2.jpg'),
                require('../assets/4.jpg'),
                require('../assets/6.jpg')
            ]
        }
    },

}
</script>

<style>
  
</style>