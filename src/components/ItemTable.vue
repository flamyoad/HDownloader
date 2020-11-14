<template>
  <div>
    <table class="table-auto">
      <thead>
        <tr class="bg-purple-900 text-white">
          <th class="px-4 py-2">Icon</th>
          <th class="px-4 py-2">Title</th>
          <th class="px-4 py-2">Pages</th>
          <th class="px-4 py-2">State</th>
          <th class="px-4 py-2">Progress</th>
        </tr>
      </thead>

      <tbody>
        <tr class="bg-gray-200 hover:bg-gray-700 text-gray-800 hover:text-gray-200">
          <td class="border-b-2 px-4 py-2">
            <img src="@/assets/nhentai.svg" width="32" height="32" />
          </td>
          <td class="px-4 py-2 truncate">
            [Urakan] Boku no SeFre wa Haha to Oba | My Mom and My Aunt Are my
            Sex Friends[English][Amoskandy]
          </td>
          <td class="px-4 py-2 text-center">33</td>
          <td class="px-4 py-2 text-center">Queued</td>
          <td class="px-4 py-2 text-center">15/33</td>
        </tr>

      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "ItemTable",
};
</script>

<style lang="scss" scoped>
  tr {
    @apply cursor-default
  }
</style>
