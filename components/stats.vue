<template>
  <div
    class="grid grid-cols-2 gap-2 sm:grid-cols-2 md:grid-cols-4 lg:grid-cols-4 xl:grid-cols-4"
  >
    <div
      class="bg-red-500 dark:bg-indigo-800 transition-all duration-300 text-white dark:text-red-500 px-4 py-10 rounded-lg shadow"
    >
      <p class="text-3xl font-bold">
        <number
        class="bold transition"
        :class="{scaleBig: scaleClass}"
        ref="number2"
        :from=stats.positif-50
        :format="theFormat"
        :to=stats.positif
        :duration="duration"
        easing="Circ.easeIn"/>
      </p>
      <p>Terkonfirmasi</p>
    </div>
    <div
      class="bg-blue-500 dark:bg-indigo-800 transition-all duration-300 text-white dark:text-blue-500 px-4 py-10 rounded-lg shadow"
    >
      <p class="text-3xl font-bold">
        <number
        class="bold transition"
        :class="{scaleBig: scaleClass}"
        ref="number2"
        :from=stats.dirawat-20
        :format="theFormat"
        :to=stats.dirawat
        :duration="duration"
        easing="Circ.easeIn"/>
      </p>
      <p>Dirawat</p>
    </div>
    <div
      class="bg-green-500 dark:bg-indigo-800 transition-all duration-300 text-white dark:text-green-500 px-4 py-10 rounded-lg shadow"
    >
      <p class="text-3xl font-bold">
        <number
        class="bold transition"
        :class="{scaleBig: scaleClass}"
        ref="number2"
        :from=stats.sembuh-20
        :format="theFormat"
        :to=stats.sembuh
        :duration="duration"
        easing="Circ.easeIn"/>
      </p>
      <p>Sembuh</p>
    </div>
    <div
      class="bg-gray-600 dark:bg-indigo-800 transition-all duration text-white  px-4 py-10 rounded-lg shadow"
    >
      <p class="text-3xl font-bold">
        <number
        class="bold transition"
        :class="{scaleBig: scaleClass}"
        ref="number2"
        :from=stats.meninggal-20
        :format="theFormat"
        :to=stats.meninggal
        :duration="duration"
        easing="Circ.easeOut"/>
      </p>
      <p>Meninggal</p>
    </div>
  </div>
</template>

<script>
import Vue from 'vue'
import VueNumber from 'vue-number-animation'
 
Vue.use(VueNumber)
export default {
  props: ["stats"],
  data() {
    return {
      duration: 3,
      scaleClass: false
    };
  },
  methods: {
    theFormat(number) {
      return new Intl.NumberFormat('id-ID').format(number);
    },
  }
};
</script>

<style></style>
