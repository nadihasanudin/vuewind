```vue
<script setup>
import ProductCard from "@/components/ProductCard.vue";

const daftarProduk = [
  {
    id: 1,
    nama: "Kaos Sekolah",
    harga: 75000,
    gambar: "kaossekolah.jpeg",
  },
  {
    id: 2,
    nama: "Topi Sekolah",
    harga: 35000,
    gambar: "Topi.jpeg",
  },
  {
    id: 3,
    nama: "Tas Sekolah",
    harga: 120000,
    gambar: "TasSekolah.jpeg",
  },
];
</script>

<template>
  <main class="min-h-screen bg-gray-100 px-6 py-12">
    <div class="mx-auto max-w-6xl">
      <div class="mb-10 text-center">
        <p
          class="mb-2 text-sm font-semibold uppercase tracking-widest text-blue-600"
        >
          SMK YADIKA SOREANG
        </p>

        <h1 class="text-4xl font-bold text-gray-900">Produk Kami</h1>

        <p class="mt-3 text-gray-600">
          Temukan berbagai kebutuhan sekolah di sini.
        </p>
      </div>

      <div class="grid grid-cols-1 gap-6 sm:grid-cols-2 md:grid-cols-3">
        <ProductCard
          v-for="produk in daftarProduk"
          :key="produk.id"
          :nama="produk.nama"
          :harga="produk.harga"
          :gambar="produk.gambar"
        />
      </div>
    </div>
  </main>
</template>
```
