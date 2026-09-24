<script setup>
import landingImage from "@/assets/background.jpeg";
</script>

<template>
  <main
    class="min-h-screen bg-cover bg-center bg-fixed"
    :style="{ backgroundImage: `url(${landingImage})` }"
  >
    <!-- OVERLAY -->
    <div class="fixed inset-0 -z-10 bg-black/60"></div>

    <!-- HERO -->
    <section class="relative">
      <div
        class="mx-auto flex min-h-[75vh] max-w-6xl items-center justify-center px-6 py-16"
      >
        <div class="text-center text-white">
          <p class="mb-4 text-sm font-semibold uppercase tracking-[0.25em]">
            SMK YADIKA SOREANG
          </p>

          <h1 class="mb-6 text-4xl font-bold md:text-6xl">
            Selamat Datang di

            <span class="block text-blue-300"> Online Shop Sekolah </span>
          </h1>

          <p class="mx-auto mb-8 max-w-2xl text-lg leading-relaxed">
            Belanja gampang, sekolah senang. Temukan berbagai produk sekolah
            dengan mudah dan nyaman.
          </p>

          <div class="flex flex-col justify-center gap-4 sm:flex-row">
            <RouterLink
              to="/product"
              class="rounded-lg bg-blue-600 px-7 py-3 font-semibold text-white shadow-lg transition hover:-translate-y-1 hover:bg-blue-700"
            >
              Lihat Produk
            </RouterLink>

            <RouterLink
              to="/about"
              class="rounded-lg border border-white px-7 py-3 font-semibold text-white transition hover:-translate-y-1 hover:bg-white hover:text-gray-900"
            >
              Tentang Kami
            </RouterLink>
          </div>
        </div>
      </div>
    </section>

    <!-- VIDEO -->
    <section class="relative px-6 py-16">
      <div class="mx-auto max-w-5xl">
        <!-- JUDUL -->
        <div class="mb-10 text-center text-white">
          <p
            class="mb-3 text-sm font-semibold uppercase tracking-[0.25em] text-blue-300"
          >
            VIDEO KAMI
          </p>

          <h2 class="text-3xl font-bold md:text-4xl">
            Kenali Online Shop Kami 🎬
          </h2>

          <p class="mx-auto mt-4 max-w-2xl text-gray-200">
            Simak video berikut untuk mengenal lebih dekat SMK YADIKA SOREANG
            dan online shop sekolah kami.
          </p>
        </div>

        <!-- VIDEO CARD -->
        <div
          class="mx-auto max-w-4xl overflow-hidden rounded-2xl border border-white/20 bg-black/70 p-3 shadow-2xl backdrop-blur-sm"
        >
          <video
            class="block aspect-video w-full rounded-xl"
            controls
            preload="metadata"
          >
            <source src="/video.mp4" type="video/mp4" />

            Browser kamu tidak mendukung pemutar video.
          </video>
        </div>
      </div>
    </section>

    <!-- FOOTER -->
    <footer
      class="border-t border-white/10 bg-black/40 px-6 py-8 text-center text-white backdrop-blur-sm"
    >
      <p class="text-sm">© 2026 SMK YADIKA SOREANG-ONLINESHOP</p>

      <p class="mt-2 text-xs text-gray-300">Belanja gampang, sekolah senang.</p>
    </footer>
  </main>
</template>
