<template>
  <button class="btn rounded-pill">
    <slot></slot>
  </button>
</template>

<script setup>
defineProps({
  propA: String,
  propB: { type: Boolean, required: true, default: false },
});
</script>



