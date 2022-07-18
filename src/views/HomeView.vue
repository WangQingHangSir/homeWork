<template>
  <div class="home">
    <wqhButton>默认按钮</wqhButton>
    <wqhButton type="primary">成功按钮</wqhButton>
    <wqhButton type="danger">危险按钮</wqhButton>
    <wqhButton type="warning">警告按钮</wqhButton>
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
