<template>
  <div>
    <h2>Parent</h2>
    <article class="is-flex">
      <p>{{ `Count is ${count}` }}</p>
    </article>
    <br>
    <Child  :count="count"
            @update:count="incrementCount"/>
    <!-- <Child v-model:count="count"/> -->
  </div>
</template>

<script setup>
import { ref } from "vue"
import Child from "./Child.vue"

let count = ref(0)

function incrementCount() {
  count.value++
}
</script>