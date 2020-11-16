<template>
  <span
    class="text-white mr-2 bg-red-900 hover:bg-red-700 cursor-default rounded py-1 px-2 mb-1 font-sans"
  >
    {{ tagName }}
  </span>
</template>

<script>
export default {
  name: "ItemTag",
  props: {
    tagName: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped></style>
