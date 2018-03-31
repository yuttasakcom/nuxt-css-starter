<template>
  <header class="header">
    <div>
      <Brand text="uHost" />
    </div>
    <Nav :items="items" text-align="right" />
  </header>
</template>

<script>
import Brand from '@/components/header/Brand'
import Nav from '@/components/header/Nav'
export default {
  components: {
    Brand,
    Nav
  },
  data() {
    return {
      items: [
        {
          text: 'Package',
          link: '/package'
        },
        {
          text: 'Order',
          link: '/order'
        },
        {
          text: 'Start Hosting',
          link: '/hosting',
          cta: true
        }
      ]
    }
  }
}
</script>

<style scoped>
header {
  width: 100%;
  background: #2ddf5c;
  padding: 8px 16px;
  box-shadow: 0 2px 10px #7c7c7c;
}

header > div {
  display: inline-block;
  vertical-align: middle;
}
</style>
