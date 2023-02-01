<script setup>
const columns = [
  {
    name: 'title',
    required: true,
    label: 'タイトル',
    align: 'left',
    field: row => row.title,
    format: val => `${val}`,
    sortable: true
  },
  {
    name: 'comment',
    required: true,
    label: 'コメント',
    align: 'left',
    field: row => row.comment,
    format: val => `${val}`,
    sortable: true
  },
]
const rows = [
  { title: 'no title', comment: 'なにも意味のないコメント' },
  { title: 'タイトルA', comment: 'なにも意味をなさないタイトル' },
]
</script>

<template>
  <div class="q-pa-md">
    <q-table
      title="サンプルテーブル"
      :rows="rows"
      :columns="columns"
      row-key="title"
    />
  </div>
</template>
