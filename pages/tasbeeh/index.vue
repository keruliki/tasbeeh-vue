<template>
  <div class="h-screen flex flex-col">
    <div class="mt-14 text-center">
      <h1 class="text-3xl font-bold">Tasbeeh</h1>
    </div>
    <div class="h-full flex flex-col justify-center items-center">
      <div class="w-1/2 rounded-xl bg-green-300 p-8">
        <div class="mb-28 p-4 rounded-lg bg-white">
          <p class="text-right text-5xl font-bold">{{ count ? count : 0 }}</p>
        </div>
        <div class="w-full flex justify-center">
          <button class="rounded-full bg-gray-400 w-20 h-20" @click="addCount">
            +
          </button>
        </div>
      </div>
    </div>
    <div class="pt-2 pb-8 px-6  bg-gray-100 shadow-md flex gap-4">
        <nuxt-link to="/" class=" bg-blue-600 px-3 py-3 rounded-md w-full text-white font-bold text-base text-center">
            Kembali
        </nuxt-link>
      <button
        @click="resetCount"
        class="bg-green-600 px-3 py-3 rounded-md w-full text-white font-bold text-base "
      >
        Mula Semula
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      count: 0,
    };
  },

  methods: {
    addCount() {
      this.count++;
    },
    resetCount() {
      this.count = 0;
    },
  },
};
</script>

<style></style>
