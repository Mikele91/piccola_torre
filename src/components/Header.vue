<template>
    <header >
        <section>
            <div class="header_container d-flex  justify-content-between align-items-center">
                <!-- Bootstrap nav -->

                
                <nav class="navbar navbar-expand-md navbar-light ">

                    <div class="container-fluid">
                        <img src="../assets/logo_torre_vettori.png" alt="">
                        
                    
                        <div class="collapse navbar-collapse" id="navbarSupportedContent">
                            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                                <li class="nav-item">
                                <a class="nav-link active" aria-current="page" href="#">La Piccola Torre</a>
                                </li>
                                
                                <!-- <li class="nav-item dropdown">
                                <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                                    Le nostre Camere
                                </a>
                                <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                                    <li><a class="dropdown-item" href="#">Camera Gialla</a></li>
                                    <li><a class="dropdown-item" href="#">Camera Blue</a></li>
                                    <li><hr class="dropdown-divider"></li>
                                    <li><a class="dropdown-item" href="#">Primo Piano </a></li>
                                </ul>
                                </li> -->
                            </ul>
                        </div>
                    </div>
                </nav>
                <!--/ Bootstrap nav -->
                <InfoContacts/>

            </div>
            
        </section>
    </header>
</template>


<script>
import InfoContacts from './nanoComponents/InfoContacts.vue';
export default {
name: 'Header',
components:{
    InfoContacts
}
}
</script >

<style lang="scss" scoped>

    header{
        max-width:75rem;
         margin:auto
    }
    img{
        height:100px;
        
    }
</style> 
