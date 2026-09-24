<template>
  <main class="min-h-screen bg-gray-100">
    <!-- HEADER -->
    <section
      class="bg-gradient-to-r from-blue-700 via-indigo-600 to-purple-600 px-6 py-16 text-center text-white"
    >
      <h1 class="text-4xl font-extrabold md:text-5xl">Hubungi Kami</h1>

      <p class="mx-auto mt-4 max-w-2xl text-lg text-blue-100">
        Punya pertanyaan atau ingin mengetahui lebih lanjut? Jangan ragu untuk
        menghubungi kami.
      </p>
    </section>

    <!-- CONTENT -->
    <section class="mx-auto max-w-6xl px-6 py-12">
      <div class="grid gap-8 md:grid-cols-2">
        <!-- INFO KONTAK -->
        <div
          class="rounded-2xl bg-white p-8 shadow-lg transition duration-300 hover:-translate-y-1 hover:shadow-2xl"
        >
          <h2 class="mb-6 text-2xl font-bold text-gray-900">
            📞 Informasi Kontak
          </h2>

          <div class="space-y-5">
            <!-- ALAMAT -->
            <div class="flex items-start gap-4 rounded-xl bg-blue-50 p-4">
              <div class="text-3xl">📍</div>

              <div>
                <h3 class="font-bold text-gray-900">Alamat</h3>

                <p class="text-gray-600">Jalan sini deket situ</p>
              </div>
            </div>

            <!-- TELEPON -->
            <div class="flex items-start gap-4 rounded-xl bg-green-50 p-4">
              <div class="text-3xl">📱</div>

              <div>
                <h3 class="font-bold text-gray-900">Telepon</h3>

                <p class="text-gray-600">(+62) 89555532444</p>
              </div>
            </div>

            <!-- EMAIL -->
            <div class="flex items-start gap-4 rounded-xl bg-purple-50 p-4">
              <div class="text-3xl">✉️</div>

              <div>
                <h3 class="font-bold text-gray-900">Email</h3>

                <p class="break-all text-gray-600">
                  smkyadikasoreang@gmail.com
                </p>
              </div>
            </div>
          </div>

          <!-- PESAN TAMBAHAN -->
          <div
            class="mt-8 rounded-xl bg-gradient-to-r from-blue-600 to-indigo-600 p-6 text-white"
          >
            <h3 class="text-xl font-bold">SMK YADIKA SOREANG</h3>

            <p class="mt-2 text-blue-100">
              Belanja gampang, sekolah senang! 🎓
            </p>
          </div>
        </div>

        <!-- FORM -->
        <div
          class="rounded-2xl bg-white p-8 shadow-lg transition duration-300 hover:shadow-2xl"
        >
          <h2 class="mb-2 text-2xl font-bold text-gray-900">💬 Kirim Pesan</h2>

          <p class="mb-6 text-gray-500">
            Isi formulir berikut untuk menghubungi kami.
          </p>

          <form class="space-y-5">
            <!-- NAMA -->
            <div>
              <label class="mb-2 block font-semibold text-gray-700">
                Nama
              </label>

              <input
                type="text"
                placeholder="Masukkan nama kamu"
                class="w-full rounded-xl border border-gray-300 px-4 py-3 outline-none transition focus:border-blue-500 focus:ring-2 focus:ring-blue-200"
              />
            </div>

            <!-- EMAIL -->
            <div>
              <label class="mb-2 block font-semibold text-gray-700">
                Email
              </label>

              <input
                type="email"
                placeholder="Masukkan email kamu"
                class="w-full rounded-xl border border-gray-300 px-4 py-3 outline-none transition focus:border-blue-500 focus:ring-2 focus:ring-blue-200"
              />
            </div>

            <!-- PESAN -->
            <div>
              <label class="mb-2 block font-semibold text-gray-700">
                Pesan
              </label>

              <textarea
                rows="5"
                placeholder="Tulis pesan kamu di sini..."
                class="w-full resize-none rounded-xl border border-gray-300 px-4 py-3 outline-none transition focus:border-blue-500 focus:ring-2 focus:ring-blue-200"
              ></textarea>
            </div>

            <!-- BUTTON -->
            <button
              type="submit"
              class="w-full rounded-xl bg-gradient-to-r from-blue-600 to-indigo-600 px-6 py-3 font-bold text-white shadow-md transition duration-300 hover:-translate-y-1 hover:shadow-xl"
            >
              🚀 Kirim Pesan
            </button>
          </form>
        </div>
      </div>
    </section>
  </main>
</template>
