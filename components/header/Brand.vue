<template>
  <nuxt-link to="/" tag="a" class="brand">{{ text }}</nuxt-link>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
a.brand {
  color: #0e4f1f;
  text-decoration: none;
  font-weight: bold;
  font-size: 22px;
}
</style>
