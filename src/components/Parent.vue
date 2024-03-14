<template>
  <div>
    <article class="is-flex">
      <p>{{ `Parent Count is ${count}` }}</p>
    </article>
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