<template>
    <div>
        <h1> {{restaurantName}} </h1>
        <h4> {{subName}} </h4>
    </div>
</template>
    
    <script>
    
    export default{
        name: 'HeaderTop',
        props:{
            restaurantName: String,
            subName:String
        }
    }
    
    </script>
    
    <style scoped>
    
    div{
        text-align: center;
    }
    
    </style>