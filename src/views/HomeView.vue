<template>
  <div class="home">
    <wqh-table :column="column" checkbox index></wqh-table>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      column: [
        {
          label: 'URL地址',
          type: 'function',
          prop: 'date',
          callback: (data) => {
            return `<a href="https://www.baidu.com">${data.name}</a>`
          }
        },
        { label: '姓名', prop: 'name' },
        { label: '地址', prop: 'address' },
        { label: '性别', prop: 'sex' }
      ]
    }
  },
  components: {
    wqhTable: () => import('../components/table/index.vue')
  },
  methods: {}
}
</script>
