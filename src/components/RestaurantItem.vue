<template>

    <div :class="item.is_it_special ? 'red': 'pink' ">
        <h2> {{item.item_name}}&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{{item.price}}$</h2>
        <h4>
            Taste:{{item.taste}}&nbsp;&nbsp;&nbsp;&nbsp;Time to cook:{{item.time_to_cook}}min
        </h4>
    </div>

</template>

<script>


export default{
    name: 'RestaurantItem',
    props:{
        item: Array
    }
}


</script>

<style scoped>


h4{
    margin: 2px;
}

div{
    background-color: #ffb89e;
    color: black;
    padding: 1em;
}

.red{
background-color: orangered !important;

}
.pink{
    color: rgb(197, 81, 164);
}


</style>