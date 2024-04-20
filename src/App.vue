<template>
  <h1>{{ title }}</h1>
  <div>
    <label for="search" class="block text-sm font-medium leading-6 text-gray-900">Quick search</label>
    <div class="relative mt-2 flex items-center">
      <input type="text" ref="name" name="search" id="search" class="block w-full rounded-md border-0 py-1.5 pr-14 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6" />
      <div class="absolute inset-y-0 right-0 flex py-1.5 pr-1.5">
        <kbd class="inline-flex items-center rounded border border-gray-200 px-1 font-sans text-xs text-gray-400">⌘K</kbd>
      </div>
    </div>
  </div>
  <button type="button" @click="handleClick" class="inline-flex items-center gap-x-1.5 rounded-md bg-indigo-600 px-2.5 py-1.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">
    Click Me
    <CheckCircleIcon class="-mr-0.5 h-5 w-5" aria-hidden="true" />
  </button>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      title: 'My First Vue App 1'
    }
  },
  methods: {
    handleClick() {
      console.log(this.$refs.name);
      this.$refs.name.classList.add('bg-black');
    }
  }
}
</script>


<style lang="css">
@import 'style.css';
</style>