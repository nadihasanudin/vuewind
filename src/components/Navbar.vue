<template>
  <nav
    class="flex items-center justify-between bg-gray-900 px-8 py-4 text-white shadow-lg"
  >
    <h2 class="text-xl font-bold">SMK YADIKA SOREANG-ONLINESHOP</h2>

    <div class="flex gap-6">
      <RouterLink to="/" class="font-medium transition hover:text-blue-400">
        Landing
      </RouterLink>

      <RouterLink
        to="/product"
        class="font-medium transition hover:text-blue-400"
      >
        Product
      </RouterLink>

      <RouterLink
        to="/about"
        class="font-medium transition hover:text-blue-400"
      >
        About
      </RouterLink>

      <RouterLink
        to="contact"
        class="font-medium transition hover:text-blue-400"
      >
        Contact
      </RouterLink>
    </div>
  </nav>
</template>
