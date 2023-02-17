<template>
    <section >
        <div class="hero d-none d-sm-block">
            <div id="carouselHero" class="carousel slide" data-bs-ride="carousel">
                <div class="carousel-indicators">
                    <button type="button" data-bs-target="#carouselHero" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
                    <button type="button"  v-for="(elm, i) in 9" :key="i" data-bs-target="#carouselHero" :data-bs-slide-to="i+1" :aria-label="`Slide${i+1}`"></button>
                </div>
                <div class="carousel-inner">
                    <div class="img_bg carousel-item active">
                        <img src="../../assets/img/bisceglie.jpg"  class="d-block w-100" alt="../../assets/img/bisceglie1.jpg">
                    </div>
                    <div class="img_bg carousel-item"  v-for="(elm, i) in 9" :key="i">
                        <img :src="require(`../../assets/img/bisceglie${i+1}.jpg`)"  class="d-block w-100" :alt="require(`../../assets/img/bisceglie${i+1}.jpg`)">
                    </div>
                
                </div>
                <button class="carousel-control-prev" type="button" data-bs-target="#carouselHero" data-bs-slide="prev">
                    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Previous</span>
                </button>
                <button class="carousel-control-next" type="button" data-bs-target="#carouselHero" data-bs-slide="next">
                    <span class="carousel-control-next-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Next</span>
                </button>
            </div>

            <!-- <div class="img_bg" v-for="(elm, i) in 9" :key="i">
                <img :src="require(`../../assets/img/bisceglie${i+1}.jpg`)" alt="" >
            </div> -->
        </div>
        
    </section>
</template>

<script>
export default {
data(){
    return {
        images:["bisceglie"],
    }
},
name: 'Hero',
}
</script >

<style lang="scss" scoped>

    .hero{
        max-width:75rem;
        margin:auto;
        box-shadow: 5px 5px 15px 5px #454545;
        border-radius: .625rem;

    }
    .img_bg{
        
        height: 500px;
        background-size: cover ;
        background-position: center;
        img{
            border-radius: .625rem;
            width: 100%;
            height: 100%;
        }
    }
</style> 


