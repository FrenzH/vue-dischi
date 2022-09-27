<template>
    <div class="album-container">
    <div class="row">
        <div v-for="album in albums" :key="album.title"  class="ac-fifth-col">
            
            <CardComponent :info="album" />
        </div>
    </div>
 </div>
</template>

<script>
import CardComponent from './CardComponent.vue'
export default {
    name: 'AlbumContainerComponent',
    props: {
        albums: Array
    }, 
    components: {
        CardComponent 
    },
}
</script>

<style lang="scss" scoped>


.album-container{
    padding-top: 50px;
    padding-bottom: 50px;
    max-width: 1200px;
    margin: auto;
    .row{
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 10px;
    }
}
.ac-fifth-col{
    width: calc(100% / 6);
}
</style>