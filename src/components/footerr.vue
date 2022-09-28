

<template>
  <div class="spacing">
    <p >Iteracion 3:</p>
    <h5 v-if="showUp===true">Muestrate como true</h5>
    <h5 v-else>Muestrate como false!</h5>
  </div>
  <div>   

  </div>

    <ul>
      <li class="footer">Iteración 4:</li>
  <li class="footer" v-for="(data, index) in datas" v-bind:key="index">
    {{ data.tittle }}-{{ data.description }}-{{ data.content }}
  </li>
  </ul>

  
</template>

<script setup>
import { ref } from "vue";

const datas = ref([
  { tittle: "AAA", description: "BBB", content: "CCC" },
  { tittle: "XXX", description: "YYY", content: "ZZZ" },
  { tittle: "DDD", description: "EEE", content: "FFF" },
]);

const showUp = ref(true);


</script>

<style scoped>
  .footer{
    list-style-type: none;
    font-size: 15px;
  }

  .spacing{
    margin-top:20px;
    margin-bottom: 20px;
  }
</style>
