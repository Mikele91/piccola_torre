<template>
    <div class="rooms ">
        <h2 class=" text-center py-2">Le nostre camere</h2>
        <section class="rooms_top ">
            <div class="row justify-content-md-between justify-content-sm-center">
                    <CardRoom @buttonEvent="showCarosel" v-for="(info, index) in caroselRooms" :key="index" :info="info"  />
            </div>
        </section>

        <section class="rooms_bottom">
            <InfoCarousel  :InfoCarousel="caroselRoomsActive" />
        </section>
    </div>
</template>

<script>
import CardRoom from '../nanoComponents/CardRoom.vue'
import InfoCarousel from '../nanoComponents/InfoCarousel.vue'
export default {
    name:"Rooms",
    components:{
        CardRoom,
        InfoCarousel
    },
data(){
        return{
            caroselRooms:[
                {
                title:"Camera Blue",
                text: "dettagli della stanza ",
                arrayImg:["blue","blue2","blue3","blue4"],//require('./assets/images/testimonial-avata-01.jpg'),
                imgCard:require(`../../assets/imgStanza/blue.jpeg`),
                price:"prezzo della stanza",
                option:"altre opzioni",
                id:"cameraBlue",
                },
                {
                title:"Camera Gialla",
                text: "dettagli della stanza2 ",
                arrayImg:["gialla","gialla2","gialla3","gialla4"],//require('./assets/images/testimonial-avata-01.jpg'),
                imgCard:require(`../../assets/imgStanza/gialla.jpeg`),
                price:"prezzo della stanza",
                option:"altre opzioni",
                id:"cameraGialla",
                },
                {
                title:"Camera Rosso",
                text: "dettagli della stanza3 ",
                arrayImg:["red","red1","red2","red3","red4","red5","red6"],//require('./assets/images/testimonial-avata-01.jpg'),
                imgCard:require(`../../assets/imgStanza/red.jpeg`),
                price:"prezzo della stanza",
                option:"altre opzioni",
                id:"cameraRossa",
                },
            ],

            clickCard:"cameraBlue",
        
        }
        
    },
    computed:{
        //filtra l'array da inviare a InfoCarosel in base all'id ricevuto dal Emit
        caroselRoomsActive(){
            return this.caroselRooms.filter(element => element.id==this.clickCard)
        } 
    },
    methods:{
        showCarosel(result){
            this.clickCard= result
        },
    
    
    
    },

}
</script>

<style lang="scss" scoped>
    .rooms{
        
        padding: 70px 0;
        .rooms_top{
            max-width:75rem;
            margin:auto;
            justify-content: space-between;
        }
        .rooms_bottom{
            .img_bg{
            height: 500px;
            background-size: cover ;
            background-position: center;
            img{
            width: 100%;
            height: 100%;
        }
    }
        }
    }
</style> 
