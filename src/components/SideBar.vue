<template>
  <!-- todo: change back to router-link -->
  <div class="flex flex-col bg-gray-800">
    <router-link class="nav-button bg-gray-600" to="/">
      <font-awesome-icon
        icon="clock"
        class="nav-icon text-white"
        style="width: 48px; height: 36px;"
      />
    </router-link>

    <router-link class="nav-button" to="/settings">
      <font-awesome-icon
        icon="cog"
        class="nav-icon text-gray-500"
        style="width: 48px; height: 36px;"
      />
    </router-link>
  </div>
</template>

<script>
export default {
  name: "SideBar",
};
</script>

<style scoped>
.nav-button {
  @apply py-1;
}

.nav-icon {
  @apply text-3xl m-2;
}

.nav-icon:hover {
  @apply text-white;
}

</style>
