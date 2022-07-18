<template>
  <div class="home">
    <wqhButton>默认按钮</wqhButton>
    <wqhButton type="primary" round disabled size="medium">成功按钮</wqhButton>
    <wqhButton type="danger" round disabled size="small">危险按钮</wqhButton>
    <wqhButton type="warning" round disabled size="mini">警告按钮</wqhButton>
  </div>
</template>

<script>
export default {
  name: 'HomeView',
  data() {
    return {
      flag: false
    }
  },
  components: {
    wqhButton: () => import('../components/button/index.vue')
  }
}
</script>
