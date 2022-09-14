<template>
    <div class="map row">
        <div class="col-md-8 map_link">

        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3000.107536822371!2d16.502432715652432!3d41.24121541300644!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1338070ebd338c5f%3A0x199f7844e1ff39a9!2sLa%20Piccola%20Torre!5e0!3m2!1sit!2sit!4v1656588579598!5m2!1sit!2sit" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
        <div class="col-md-4 map_text text-center">
            <h3>Dove Siamo</h3>
            <p> <i>La Piccola Torre</i>  è situata nel cuore della bellissima Bisceglie a cira 200m dal mare e a soli 50 metri dal Castello Svevo. </p>
            <p>Bisceglie  si trova in una posizione strategica nel nord Barese a 30(km da Bari) Con stazione ferroviaria a 10 minuti a piedi da <i>La Piccola Torre</i>  sarà possibile raggiungere location su tutta la costiera Pugliese in maniera agevolata con Treni o auto come la splendida <a href="https://goo.gl/maps/acPTGHAE88WrxNnP7"> Polignano a Mare</a> a soli 70km  o talti altri. </p>
            <p>Posti consigliati da visitare </p>
            <ul>
                <li>1</li>
                <li>2</li>
                <li>3</li>
                <li>4</li>
                <li>5</li>
                <li>5</li>
                 <li>3</li>
                <li>4</li>
                <li>5</li>
                <li>5</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name:"Maps",

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
