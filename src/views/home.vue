<template>
  <div class="home">
    <wqh-button disabled>默认按钮</wqh-button>
    <wqh-button type="primary" round :loading="flag" @click="handleSubmit"
      >成功按钮</wqh-button
    >
    <wqh-button type="danger" suffix="tongzhi">危险按钮</wqh-button>
    <wqh-button type="warning" block>警告按钮</wqh-button>
  </div>
</template>

<script>
export default {
  name: 'home',
  data() {
    return {
      flag: false
    }
  },
  components: {
    wqhButton: () => import('../components/Button')
  },
  methods: {
    handleSubmit() {
      this.flag = true
      setTimeout(() => {
        console.log('123')
        this.flag = false
      }, 3000)
    }
  }
}
</script>
