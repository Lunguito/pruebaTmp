<script setup>
import {ref} from 'vue';
var count = ref(0)
var msg = ref("Hola Pajin")

function increment(){
    count.value++
}
function decrement(){
    count.value--
}
function alCuadrado(){
  count.value = count.value*count.value;
}
function alCubo(){
  count.value = count.value*count.value*count.value;
}
function sqrt2(){
  count.value = Math.sqrt(count.value);
}
function sqrt3(){
  count.value = Math.cbrt(count.value);
}
</script>

<template>
  <header>
    <h1>¡Hola mundo!</h1>
    <h3>Count is {{ count }}</h3>
    
    <div>
      <input type="text" name="Texto" :value="msg"
        @input="event =>msg=event.target.value">
      <h2><span> Message: {{msg}}</span></h2>
    </div>
    
    <div>
      <button @click="increment">incrementar</button>
      <button @click="decrement">decrementar</button>
      <button @click="alCuadrado">elevar al cuadrado</button>
      <button @click="alCubo">elevar al alCubo</button>
      <button @click="sqrt2">sqrt2</button>
      <button @click="sqrt3">sqrt3</button>

    </div>
  </header>

  <main>
    
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

}
</style>
