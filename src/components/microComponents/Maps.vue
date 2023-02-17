<template>
    <div class="map row">
        <div class="col-md-8 map_link">

        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3000.107536822371!2d16.502432715652432!3d41.24121541300644!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1338070ebd338c5f%3A0x199f7844e1ff39a9!2sLa%20Piccola%20Torre!5e0!3m2!1sit!2sit!4v1656588579598!5m2!1sit!2sit" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
        <div class="col-md-4 map_text text-center">
            <h3>Dove Siamo</h3>
            <p> <i>La Piccola Torre</i>  è situata nel cuore della bellissima Bisceglie a cira 200m dal mare e a soli 50 metri dal Castello Svevo. </p>
            <p>Bisceglie  si trova in una posizione strategica nel nord Barese a 30(km da Bari) Con stazione ferroviaria a 10 minuti a piedi da <i>La Piccola Torre</i>  sarà possibile raggiungere location su tutta la costiera Pugliese in maniera agevolata con Treni o auto come la splendida <a href="https://goo.gl/maps/acPTGHAE88WrxNnP7"> Polignano a Mare</a> a soli 70km  o talti altri. </p>
            <p>Posti consigliati da visitare a bisceglie: </p>
            <ul>
                <li v-for="(place,index) in places" v-bind:key="index" >
                    <a v-bind:href="place.link">{{place.name}}</a>
                </li>
            </ul>
            <p>Città vicine: </p>
            <ul>
                <li v-for="(city,index) in cities" v-bind:key="index" >
                    <a v-bind:href="city.link">{{city.name}}</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name:"Maps",
    data(){
        return{
            places:[
                {
                    name:"Teatro Mediterraneo",
                    link: "https://www.google.com/maps/dir/41.2061979,16.2597532/teatro+mediterraneo+biscegkue%2B/@41.2396408,16.2286212,11z/data=!3m1!4b1!4m9!4m8!1m1!4e1!1m5!1m1!1s0x133806e623237f79:0xdc781502cf553fb!2m2!1d16.4765927!2d41.2554017"
                },
                {
                    name:"Basilica Concattedrale S. Pietro Apostolo",
                    link: "https://www.google.com/maps/place/Basilica+Concattedrale+S.+Pietro+Apostolo/@41.2421361,16.501671,17z/data=!3m1!4b1!4m5!3m4!1s0x1338070f1b9d85fb:0x434d4f54e9fa4fff!8m2!3d41.2420929!4d16.5038449"
                },
                {
                    name:"Chiesa San Giuseppe",
                    link: "https://www.google.com/maps/place/Chiesa+San+Giuseppe/@41.2426934,16.4930619,17z/data=!3m1!4b1!4m5!3m4!1s0x1338074781ee36eb:0x3e4637342f58ecef!8m2!3d41.2426895!4d16.4975466"
                },
                {
                    name:"Dolmen della Chianca",
                    link: "https://www.google.com/maps/place/Dolmen+della+Chianca+-+Bisceglie/@41.1941148,16.4851211,17z/data=!3m1!4b1!4m5!3m4!1s0x13380887565228d5:0xd40c7c6cc47503dd!8m2!3d41.1941108!4d16.4873098"
                }
            ],
            cities:[
                {
                    name:"Polignano",
                    link: "https://www.google.com/maps/place/70044+Polignano+a+Mare+BA/@40.9962248,17.2077652,15z/data=!3m1!4b1!4m5!3m4!1s0x1347cbeb9e80f67b:0x9bbe6b6e25a97601!8m2!3d40.9948946!4d17.22261"
                },
                {
                    name:"Monopoli",
                    link: "https://www.google.com/maps/place/70043+Monopoli+BA/@40.9500903,17.2801555,15z/data=!3m1!4b1!4m5!3m4!1s0x13463531e12fff0f:0x3279d7289d5ffde2!8m2!3d40.9525166!4d17.2985559"
                },
                {
                    name:"Lecce",
                    link: "https://www.google.com/maps/place/73100+Lecce+LE/@40.3541621,18.1567849,14z/data=!3m1!4b1!4m5!3m4!1s0x13442ee42f2d1109:0x9b5b5a4c6ab377f0!8m2!3d40.3515155!4d18.1750161"
                },
                {
                    name:"Vieste",
                    link: "https://www.google.com/maps/place/71019+Vieste+FG/@41.8823589,16.1644179,15z/data=!3m1!4b1!4m5!3m4!1s0x1337c811298cb055:0xa4fd495c9ae867ae!8m2!3d41.8824764!4d16.1767489"
                },
            
            ]

        }
    },

}
</script>

<style lang="scss" scoped>
.map{
    max-width:75rem;
    margin:auto;
    height: 31.25rem;
    .map_text{
        height: 100%;
        overflow-y: scroll ;
    }
    
}

</style>
