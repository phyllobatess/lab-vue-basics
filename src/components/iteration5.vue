<template>
    <div class="container" :class="changeColor ? 'is-red' : 'is-orange' ">

        <h1>Cambiemos el color del fondo pulsando el boton:</h1>
        <button @click="changeColorFunction">click para cambiar color!</button>
    </div>
</template>

<script setup>
import { ref } from 'vue';
// Iteration 1:
const changeColor = ref(true);
function changeColorFunction() {
    changeColor.value = !changeColor.value;
}
</script>
<style>
    h1{
        text-align: center;
        color:black;
    }
    .container{
        min-height: 20rem;
        display:flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }


    .is-red{
        background-color: red;
    }

    .is-orange{
        background-color: orange;
    }

</style>