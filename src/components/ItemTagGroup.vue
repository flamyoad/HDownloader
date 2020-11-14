<template>
  <div class="flex flex-wrap">
    <span class="text-white font-semibold mr-4 my-auto">
      {{ categoryName }}
    </span>

    <ItemTag v-for="tag in tagList" 
    :key="tag.id" 
    :tagName="tag.name" />
  </div>
</template>

<script>
import ItemTag from "@/components/ItemTag.vue";

export default {
  name: "ItemTagGroup",
  components: {
    ItemTag,
  },
  props: {
    categoryName: {
      type: String,
      required: true,
    },
    tagList: {
      type: Array,
      required: true,
      default: () => [],
    },
  },
};
</script>
