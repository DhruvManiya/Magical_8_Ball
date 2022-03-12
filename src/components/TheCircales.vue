<template>
    <div class="circales" >
    <p>{{ answer }}</p>
    </div>
</template>


<script>

export default {

props:['answer'],
}
</script>



<style>

p{

    font-size: 30px;
    height: 75px;
    width: 80%;
    background-color: black;
    color: rgb(255, 88, 27);
    z-index: 1;
    padding: 5px 15px;
    box-shadow: inset 0 0 10px rgba(256, 256, 256,0.7);
    
}


.circales{
    height: 300px;
    width: 300px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 50%;
    background: #ffffff;
    transform: translate(150px,-495px) ; 
               
}
</style>