<template>
  <div class="bg-gray-800 h-full">
    <div class="p-2">
      <img src="@/assets/girl.jpg" class="h-64 w-full object-contain rounded-lg" />
      <p class="text-white font-bold leading-tight py-4">
        [Urakan] Boku no SeFre wa Haha to Oba | My Mom and My Aunt Are my Sex
        Friends[English][Amoskandy]
      </p>

      <p class="text-gray-400 font-bold leading-tight py-2 mb-2">
        [U羅漢] 僕のセフレは母と叔母[英訳]
      </p>

      <ItemTagGroup categoryName="Parodies" :tagList="parodies"></ItemTagGroup>
      <ItemTagGroup categoryName="Tags" :tagList="tags"></ItemTagGroup>
      <ItemTagGroup categoryName="Artists" :tagList="artists"></ItemTagGroup>
      <ItemTagGroup
        categoryName="Languages"
        :tagList="languages"
      ></ItemTagGroup>
      <ItemTagGroup
        categoryName="Categories"
        :tagList="categories"
      ></ItemTagGroup>
      <ItemTagGroup categoryName="Pages" :tagList="pages"></ItemTagGroup>
    </div>
    <ItemOverviewBottomNav />
  </div>
</template>

<script>
import ItemTagGroup from "@/components/ItemTagGroup.vue";
import ItemOverviewBottomNav from "@/components/ItemOverviewBottomNav";

export default {
  name: "ItemOverview",
  components: {
    ItemTagGroup,
    ItemOverviewBottomNav,
  },

  data() {
    return {
      parodies: [{ id: 1, name: "original" }],
      tags: [
        { id: 1, name: "big breasts" },
        { id: 2, name: "group" },
        { id: 3, name: "sole female" },
      ],
      artists: [{ id: 1, name: "urakan" }],
      languages: [{ id: 1, name: "chinese" }],
      categories: [
        { id: 1, name: "doujinshi" },
        { id: 2, name: "translated" },
      ],
      pages: [{ id: 1, name: "33" }],
    };
  },
};
</script>
