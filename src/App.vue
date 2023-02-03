<!-- eslint-disable max-len -->
<template>
  <div class="bg-white">
    <div class="py-24 px-6 sm:px-6 sm:py-32 lg:px-8">
      <div class="mx-auto max-w-2xl text-center">
        <h2 class="text-4xl font-bold tracking-tight text-gray-900">
          {{ theCook }} mikor jön a kaja?
        </h2>
        <p class="mx-auto mt-6 max-w-xl text-lg leading-8 text-gray-600">
          Kérdezd meg {{ theCook }}tól mikor jön meg a kaja!
        </p>
        <div class="mt-10 flex items-center justify-center gap-x-6">
          <a
          v-on:click="isHidden = false, num = Math.floor(Math.random() * (answers.length - 0)) + 0"
            href="#"
            class="rounded-md bg-indigo-600 px-3.5 py-1.5 text-base font-semibold leading-7 text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
            >Na mikor?!</a
          >
        </div>
        <div v-if="!isHidden" className="mt-6 text-lg">{{ theCook }}: {{ answers[num] }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      theCook: 'Szilárd',
      isHidden: true,
      answers: ['Nem tudom.', '40 perc.', '100 perc múlva', 'Késik', 'Linia ocupata, s most az előbb becsenget de basznak rá felvenni', 'Meg se lehet kérdezni mivan', '30 sec csengetés után sehol semmi', 'Éhezni fogunk ezek is megvesztek, hogy hull a hó 110 percet adtak', 'Valamikor'],
      num: Number,
    };
  },
};

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
