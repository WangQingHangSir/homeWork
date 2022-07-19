<template>
  <div class="home">
    <wqh-table  :column="column"></wqh-table>
  </div>
</template>

<script>

export default {
  name: 'Home',
  data () {
    return {
      column: [
        { label: '日期', prop: 'date' },
        { label: '姓名', prop: 'name' },
        { label: '地址', prop: 'address' },
        { label: '性别', prop: 'sex' }
      ]
    }
  },
  components: {
    wqhTable: () => import('../components/table/index.vue')
  },
  methods: {

  }
}
</script>
