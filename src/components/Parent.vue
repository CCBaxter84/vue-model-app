<template>
  <div>
    <h2>Parent</h2>
    <article class="is-flex">
      <p>Count: </p>
      <p>{{ count }}</p>
    </article>
    <br>
    <Child v-model:count="count"/>
  </div>
</template>

<script setup>
import { ref } from "vue"
import Child from "./Child.vue"

let count = ref(0)
</script>