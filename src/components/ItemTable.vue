<template>
  <div class="bg-gray-100">
    <table class="table-fixed width:100%">
      <thead>
        <tr class="bg-purple-900 text-white">
          <th class="header">Icon</th>
          <th class="header">Title</th>
          <th class="header">Pages</th>
          <th class="header">State</th>
          <th class="header">Progress</th>
        </tr>
      </thead>

      <tbody>
        <TableRow
          v-for="doujin in doujins"
          :key="doujin.id"
          :title="doujin.title"
          :totalPages="doujin.totalPages"
          :status="doujin.status"
          :pagesDownloaded="doujin.pagesDownloaded"
        />
      </tbody>
    </table>
  </div>
</template>

<script>
import TableRow from "@/components/TableRow.vue";

export default {
  name: "ItemTable",

  components: {
    TableRow
  },

  data: function() {
    return {
      doujins: [
        {
          id: 1,
          title:
            "[Urakan] Boku no SeFre wa Haha to Oba | My Mom and My Aunt Are my Sex Friends[English][Amoskandy]",
          totalPages: 33,
          status: "Queued",
          pagesDownloaded: "15/33",
        },

        {
          id: 2,
          title:
            "[Urakan] Boku no SeFre wa Haha to Oba | My Mom and My Aunt Are my Sex Friends[English][Amoskandy]",
          totalPages: 33,
          status: "Queued",
          pagesDownloaded: "15/33",
        },
      ],
    };
  },
};
</script>

<style scoped>
tr {
  @apply cursor-default;
}

.status-column {
  @apply px-4 py-1 my-auto text-center inline-block text-xs leading-5 font-semibold rounded-full bg-green-200 text-green-800;
}

.header {
  @apply px-4 py-2 uppercase font-semibold font-sans tracking-wider
}
</style>
