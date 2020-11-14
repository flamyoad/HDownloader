<template> 
  <div class="flex flex-row">
    <ItemTable class="w-5/8"/>
    <ItemOverview class="w-3/8"/>
  </div>
</template>

<script>
// import { component } from "vue/types/umd";
import ItemTable from "@/components/ItemTable.vue";
import ItemOverview from "@/components/ItemOverview.vue";

export default {
  name: "ListScreen",
  components: {
    ItemTable,
    ItemOverview
  },
};
</script>
