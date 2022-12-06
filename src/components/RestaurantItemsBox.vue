<template>
    <div class="itembox">


        

        <div v-for="item in items" :key="item.id" >
            <RestaurantItem :item="item"/>
        </div>

    </div>
    


</template>

<script>

    import RestaurantItem from './RestaurantItem.vue'


    export default{
        name: 'RestaurantItemsBox',
        components: {
            RestaurantItem
        },
        props:{
            
            items: Array
        }
    }

</script>

<style scoped>

.itembox{

background-color: bisque;
padding: 1em;
color: gray;
}

</style>