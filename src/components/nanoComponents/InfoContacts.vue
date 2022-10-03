<template>
    <div>
        <!-- Vertically centered scrollable modal -->
        
            <!-- Button trigger modal -->
            <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
                CONTATTACI 
            </button>
            
            <!-- Modal -->
            <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
                <div class="modal-dialog modal-dialog-centered modal-dialog-scrollable">
                    <div class="modal-content">
                    <div class="modal-header">
                        <h5 class="modal-title" id="exampleModalLabel">I nostri contatti  </h5>
                        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                    </div>
                    <div class="modal-body">
                        <ul>
                            <li><strong> Tel:</strong> <span v-on:focus="$event.target.select()" ref="myinput" readonly :value="tel">{{tel}}</span>  &nbsp;<i title="copy" class=" btn fa-regular fa-copy " @click="copy"></i></li>
                            <li><strong> Cellulare:</strong> +39 3407195072 &nbsp; <i title="copy" class="fa-regular fa-copy"></i></li>
                            <li><strong> E-mail: </strong> <i> <a href="mailto:anna_lagroia@hotmail.it"> anna_lagroia@hotmail.it </a></i>&nbsp; <i title="copy" class=" fa-regular fa-copy"></i></li>
                            <li><strong>indirizzo:</strong> Centro Storico - Strada Pastore, 4 <br> angolo Strada Sciarra - 76011 Bisceglie (BT)&nbsp; <i title="copy"  class="fa-regular fa-copy"></i></li>
                        </ul>
                    </div>
                    <div class="modal-footer">
                        <button type="button" class="btn btn-danger" data-bs-dismiss="modal">Chiudi</button>
                    </div>
                    </div>
                </div>
            </div>
        </div>

</template>

<script>
export default {
    name:"Modal",
    data(){
        return{
            tel:"080 3952399",

        }
    },
    methods:{

    copy() {
        this.$refs.myinput.focus();
        document.execCommand('copy');
    }
    }
}
</script>

<style lang="scss" scoped>
    ul{
        list-style: none;
    }
</style>
