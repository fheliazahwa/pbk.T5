<script setup>
import { ref, computed, watch, onMounted } from 'vue';

onMounted(() => {
  console.log("Aplikasi daftar peserta kelas online siap digunakan");
});
</script>

<template>
  <div>
    <h2>📚 Daftar Peserta Kelas Online</h2>
    <ul>
      <li v-for="(item, index) in peserta" :key="index">
        {{ item.name }} - {{ item.age }} tahun
      </li>
    </ul>
    <h3>👥 Total Peserta: {{ totalPeserta }}</h3>
    <button @click="addPeserta">Tambah Peserta</button>
  </div>
</template>
