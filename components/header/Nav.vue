<template>
  <nav :style='{"text-align": textAlign}'>
    <ul class="nav-items">
      <nuxt-link
        tag="li"
        class="nav-item"
        v-for="item in items"
        :key="item.text"
        :to="item.link"
        :class='{"nav-item-cta": item.cta}'
      >
        <a>{{ item.text }}</a>
      </nuxt-link>
    </ul>
  </nav>
</template>

<script>
export default {
  props: {
    items: {
      type: Array
    },
    textAlign: {
      type: String,
      default: 'right'
    }
  }
}
</script>

<style scoped>
nav {
  display: inline-block;
  width: calc(100% - 74px);
}

.nav-items {
  margin: 0;
  padding: 0;
  list-style: none;
}

.nav-item {
  display: inline-block;
  margin: 0 16px;
}

.nav-item a {
  text-decoration: none;
  color: #0e4f1f;
  font-weight: bold;
  padding: 3px;
}

.nav-item a:hover,
.nav-item a:active {
  color: white;
  border-bottom: 5px solid white;
}

.nav-item-cta a {
  color: white;
  background: #ff1b68;
  padding: 8px 16px;
  border-radius: 8px;
}

.nav-item-cta a:hover,
.nav-item-cta a:active {
  color: #ff1b68;
  background: white;
  border: none;
}
</style>

