<template>
  <div
    class="bg-gray-100 dark:bg-black transition-all duration-300 min-h-screen"
  >
    <navbar />
    <div class="container mx-auto pt-24 p-4" v-if="source">
      <stats :stats="source" />
      <!-- <cases :states="source.statewise" /> -->
      <p class="text-center">
        <a
          class=" text-center text-gray-500 dark:text-white my-8"
          href="https://apicovid19indonesia-v2.vercel.app/"
          >Sumber Data</a
        >
      </p>
    </div>
  </div>
</template>

<script>
import navbar from "~/components/navbar";
import stats from "~/components/stats";
// import cases from "~/components/cases";
import axios from "axios";
export default {
  data() {
    return {
      source: null
    };
  },
  components: {
    stats,
    // cases,
    navbar
  },
  async mounted() {
    const { data } = await axios.get(
      `https://apicovid19indonesia-v2.vercel.app/api/indonesia`
    );
    this.source = data;
  }
};
</script>
