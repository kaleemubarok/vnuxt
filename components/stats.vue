<template>
  <div
    class="grid grid-cols-2 gap-2 sm:grid-cols-2 md:grid-cols-4 lg:grid-cols-4 xl:grid-cols-4"
  >
    <div
      class="bg-red-500 dark:bg-gray-900 transition-all duration-300 text-white dark:text-red-500 px-4 py-10 rounded-lg shadow"
    >
      <p class="text-3xl font-bold">{{ stats.positif }}</p>
      <p>Terkonfirmasi</p>
    </div>
    <div
      class="bg-blue-500 dark:bg-gray-900 transition-all duration-300 text-white dark:text-blue-500 px-4 py-10 rounded-lg shadow"
    >
      <p class="text-3xl font-bold">{{ stats.dirawat }}</p>
      <p>Dirawat</p>
    </div>
    <div
      class="bg-green-500 dark:bg-gray-900 transition-all duration-300 text-white dark:text-green-500 px-4 py-10 rounded-lg shadow"
    >
      <p class="text-3xl font-bold">{{ stats.sembuh }}</p>
      <p>Sembuh</p>
    </div>
    <div
      class="bg-gray-600 dark:bg-gray-900 transition-all duration text-white  px-4 py-10 rounded-lg shadow"
    >
      <p class="text-3xl font-bold">{{ stats.meninggal }}</p>
      <p>Meninggal</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["stats"]
};
</script>

<style></style>
