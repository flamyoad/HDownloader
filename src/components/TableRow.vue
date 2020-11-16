<template>
  <tr class="bg-gray-100 hover:bg-gray-300 ">
    <td class="px-4 py-2">
      <img src="@/assets/nhentai.svg" width="32" height="32" />
    </td>
    <td class="px-4 py-2 truncate text-sm text-gray-800 hover:text-gray-900">
      {{ title }}
    </td>
    <td class="px-4 py-2 text-center text-gray-600 text-sm leading-5">
      {{ totalPages }}
    </td>
    <td>
      <div class="status-column">{{ status }}</div>
    </td>
    <td class="px-4 py-2 text-center text-gray-600 text-sm leading-5">
      {{ pagesDownloaded }}
    </td>
  </tr>
</template>

<script>
export default {
  component: "TableRow",
  props: {
    title: {
      type: String,
      required: true,
    },
    totalPages: {
      type: Number,
      required: true,
    },
    status: {
      type: String,
      required: true,
    },
    pagesDownloaded: {
      type: String,
      required: true,
    },
  },
};
</script>

<style>
tr {
  @apply cursor-default;
}

.status-column {
  @apply px-4 py-1 my-auto text-center inline-block text-xs leading-5 font-semibold rounded-full bg-green-200 text-green-800;
}
</style>
