<template>
  <div class="flex flex-row p-3 bg-gray-800">
    <label class="my-auto flex-shrink-0 text-white">Link URL</label>
    <input
      class="w-full shadow appearance-none border rounded text-gray-800 p-2 mx-4"
      placeholder="Enter your url here"
    />
    <button
      class="bg-white text-gray-800 hover:text-white hover:bg-gray-600 border-current font-bold rounded px-6 py-2 focus:outline-none"
    >
      Add
    </button>
  </div>
</template>

<script>
export default {
  name: "InputUrlField",
};
</script>
