<template>
  <div>
    <h3>Child</h3>
    <button @click="incrementCount"
            class="button">
      Increment
    </button>
    <article class="is-flex">
      <p>{{ `Count is ${count}` }}</p>
    </article>
  </div>
</template>

<script setup>
// const props = defineProps({
//   count: Number
// })

// function incrementCount() {
//   props.count++
// }

const props = defineProps({
  count: Number
})
const emit = defineEmits(['update:count'])

function incrementCount() {
  emit('update:count', props.count + 1)
}

// let count = defineModel('count')

// function incrementCount() {
//   count.value++
// }
</script>