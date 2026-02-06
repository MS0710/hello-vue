<template>
  <AdminLayout>
    <h2 class="title">工作列表</h2>

    <div class="grid">
      <div class="job" @click="$router.push('/performers')">
        <div class="jobTitle">所有表演者</div>
        <div class="jobDesc">讀取 /v1/admin/performers/all，顯示頭像與暱稱</div>
        <div class="tag">API</div>
      </div>
    </div>
  </AdminLayout>
</template>

<script setup>
import AdminLayout from '../layouts/AdminLayout.vue'
</script>

<style scoped>
.title {
  margin: 0 0 14px 0;
}

.grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 12px;
}

@media (max-width: 900px) {
  .grid { grid-template-columns: repeat(1, minmax(0, 1fr)); }
}

.job {
  border: 1px solid #eee;
  border-radius: 16px;
  padding: 16px;
  cursor: pointer;
  background: #fff;
}

.job:hover {
  border-color: rgba(174, 25, 20, 0.35);
  box-shadow: 0 8px 24px rgba(0,0,0,0.06);
}

.jobTitle {
  font-weight: 800;
  color: #111;
}

.jobDesc {
  margin-top: 6px;
  opacity: 0.8;
  font-size: 14px;
}

.tag {
  margin-top: 12px;
  display: inline-block;
  padding: 4px 8px;
  border-radius: 999px;
  border: 1px solid rgba(174, 25, 20, 0.35);
  color: #AE1914;
  font-weight: 700;
  font-size: 12px;
}
</style>
