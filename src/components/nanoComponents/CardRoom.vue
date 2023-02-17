<template>
    <!-- prima riga  -->
    <div @click="$emit('buttonEvent', info.id)" :id="info.id"  class="card  " style="width: 18rem;">
        <img :src="info.imgCard" class="card-img-top " alt="">
        <div class="card-body d-flex flex-column align-items-center">
            <h5 class="card-title"> {{info.title}} </h5>
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
    margin-bottom: 1.875rem;
    opacity: 0.8;
    transition:  0.4s;

    img{
        border-radius: 30%;
        transition:  0.4s;
    }
}
.card:hover{
    opacity: 1;
    img{
        border-radius: 10%;
    }
    
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

#cameraBlue{
    border-color:rgb(0, 153, 255) ;
    color:black;
    background-color:rgb(0, 153, 255);
}

</style> 
