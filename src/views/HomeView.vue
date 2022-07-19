<template>
  <div class="home">
    <wqh-table></wqh-table>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      flag: false
    }
  },
  components: {
    wqhTable: () => import('../components/table/index.vue')
  },
  methods: {}
}
</script>
