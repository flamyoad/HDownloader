<template>
  <div class="mt-2 flex flex-row">
    <button class="nav-button">
      <font-awesome-icon icon="download" class="button-image" />
      Start Downloading
    </button>

    <button class="nav-button">
      <font-awesome-icon icon="folder-open" class="button-image" />
      Open in file explorer
    </button>

    <button class="nav-button">
      <font-awesome-icon :icon="['fab', 'chrome']" class="button-image" />
      Open in web browser
    </button>
  </div>
</template>

<script>
export default {
  name: "ItemOverviewBottomNav",
};
</script>

<style scoped>
.nav-button {
  @apply w-1/3 bg-gray-600 text-gray-300 text-sm py-2 px-2;
}

.nav-button:hover {
  @apply bg-gray-700 text-gray-200;
}

.button-image {
  @apply block mx-auto my-2;
}
</style>
