<script setup>
import { ref } from "vue";

defineProps(["nama", "harga", "gambar"]);

const tampilNotifikasi = ref(false);

function tambahKeKeranjang() {
  // Putar suara
  const audio = new Audio("/notipdana.mpeg");
  audio.play();

  // Tampilkan notifikasi
  tampilNotifikasi.value = true;

  // Hilangkan setelah 2 detik
  setTimeout(() => {
    tampilNotifikasi.value = false;
  }, 2000);
}
</script>

<template>
  <div
    class="overflow-hidden rounded-xl bg-white shadow-md transition duration-300 hover:-translate-y-1 hover:shadow-xl"
  >
    <img :src="gambar" :alt="nama" class="h-56 w-full object-cover" />

    <div class="p-5">
      <h3 class="mb-2 text-xl font-bold text-gray-900">
        {{ nama }}
      </h3>

      <p class="text-lg font-semibold text-blue-600">
        Rp {{ harga.toLocaleString("id-ID") }}
      </p>

      <button
        @click="tambahKeKeranjang"
        class="mt-4 w-full rounded-lg bg-blue-600 px-4 py-2 font-semibold text-white transition hover:bg-blue-700"
      >
        Tambah ke Keranjang
      </button>
    </div>

    <!-- NOTIFIKASI -->
    <div
      v-if="tampilNotifikasi"
      class="fixed right-5 top-5 z-50 rounded-lg bg-green-500 px-6 py-4 font-semibold text-white shadow-xl"
    >
      🛒 {{ nama }} berhasil ditambahkan ke keranjang!
    </div>
  </div>
</template>
