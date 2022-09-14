<template>
                    <!-- prima riga  -->

                    <div  class="card" style="width: 18rem;">
                        <img :src="info.imgCard" class="card-img-top " alt="">
                            <div class="card-body">
                                <h5 class="card-title"> {{info.title}} </h5>
                                <p class="card-text">{{info.text}}</p>
                                <a @click="$emit('buttonEvent', info.id)" :id="info.id"  class="btn btn-primary">Dettagli {{info.title}} </a>
                            </div>
                    </div>

</template>

<script>

export default {
    name:"CardRoom",
    data(){
        return{
            
        }
    },
    props:{
        info:Array,
        
    },
    
}
</script>
<style lang="scss" scoped>
img{
    height: 14rem;
    padding: 8px 
}
.card{

    border: none;
}
#cameraRossa{
    border-color: #9e0028;
 
    background-color: #9e0028;
}
#cameraGialla{
    border-color:rgb(255, 208, 0) ;
    color:black;
    background-color: rgb(255, 208, 0);
}

</style> 
