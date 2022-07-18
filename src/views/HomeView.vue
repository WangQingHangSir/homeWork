<template>
  <div class="home">
    <wqhButton >默认按钮</wqhButton>
    <wqhButton  :loading="flag" @click="handleSubmit" size="medium" type="primary"  >成功按钮</wqhButton>
    <wqhButton type="danger" >危险按钮</wqhButton>
    <wqhButton type="warning" >警告按钮</wqhButton>
  </div>
</template>

<script>

export default {
  name: 'Home',
  data () {
    return {
      flag: false
    }
  },
  components: {
    wqhButton: () => import('../components/button/index.vue')
  },
  methods: {
    handleSubmit () {
      this.flag = true
      setTimeout(() => {
        console.log('123')
        this.flag = false
      }, 3000)
    }
  }
}
</script>
