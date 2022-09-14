<template>
    <main>
        <Hero/>
        <Rooms/>
        <Maps/>

    </main>
</template>

<script>
import Hero from './microComponents/Hero.vue'
import Rooms from './microComponents/Rooms.vue'
import Maps from './microComponents/Maps.vue'
export default {
name: 'Main',
components: {
    Hero, 
    Rooms,
    Maps,
}
}
</script >

<style lang="scss" scoped>
  
</style> 
