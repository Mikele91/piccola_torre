<template>
    <section class="section_carosel" >
        <div class="circle ">
            <div  @click="nextPg()">
                <i class="fa-solid fa-caret-up" ></i>
            </div>
            <div class="numb my-2">
                {{visibitily+1}}/{{carouselLength}}
            </div>
            <div @click="prevPg()">
                <i  class="fa-solid fa-caret-down" ></i>   
            </div>
        </div>

        <div v-for="(info, index) in InfoCarousel" :key="index" class="row">
            <div :id="info.id"  class="col-md-6 sez_1 text-center room_card_text">
                <h5 class="my-5">{{info.title}}</h5>
                <div class="text">
                {{info.text}}
                </div>
                <p>{{info.price}}</p>
                <p>{{info.option}}</p>
            </div>

            <div  v-show="visibitily==i" v-for="(foto,i) in info.arrayImg" :key="i" class="col-md-6 room_card_img">
                <img class="card_img" :src="require(`../../assets/imgStanza/${foto}.jpeg`)" >
                
            </div>

        </div>
    </section>
</template>

<script>

export default {
name:"Carosel",
props:{
    InfoCarousel:Array,
},
data(){
    return{
        visibitily: 0,
    }
},
watch:{
    //rimane in ascotlo delle props, quando cambia riaggiorna il valore di visibility!
    InfoCarousel(){
    this.visibitily= 0;
    }
},
computed:{
        carouselLength(){
        return this.InfoCarousel[0].arrayImg.length ;
        }, 
    },
methods:{
        nextPg(){
            //console.log(this.InfoCarousel[0].pippo);
            this.visibitily++;
            if( this.visibitily >= this.InfoCarousel[0].arrayImg.length){
                this.visibitily = 0;  
            }
        },
        prevPg(){
            this.visibitily--;
            if(this.visibitily == -1){
                this.visibitily = this.InfoCarousel[0].arrayImg.length-1;
            }
        },

    },
    
}
</script>

<style scoped lang="scss">

.section_carosel{
    position: relative;
    .circle{
        width: 6rem;
        height: 6rem;
        border-radius: 50%;
        background-color: white;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        i{
            cursor: pointer;
        }

    }
}

.room_card_img{
    .card_img{
        width: 100%;
        object-fit: cover;
        height: 500px;
        
    }

}
#cameraBlue{
    
    background-color: rgb(0, 153, 255);
}
#cameraRossa{
    
    background-color: #9e0028;
}
#cameraGialla{
    
    background-color:rgb(255, 208, 0);
}
</style>