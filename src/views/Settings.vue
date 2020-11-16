<template>
  <div class="p-4 w-full h-full">
    <div class="flex flex-row mb-4">
      <label class="w-1/10 settings-label" for="download-dir">
        Download directory
      </label>

      <input
        class="flex-1 bg-gray-200 appearance-none border-2 border-gray-200 rounded py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
        id="download-dir"
        placeholder="All downloaded items will go here"
      />

      <button v-on:click="openFolderDialog" class="focus:outline-none">
        <font-awesome-icon
          class="ml-4"
          icon="folder-open"
          style="font-size: 28px;"
        />
      </button>
    </div>

    <div class="flex flex-row mb-4">
      <label class="settings-label" for="simultaneous-download"
        >Simultaneous download limit</label
      >
      <input
        class="bg-gray-200 appearance-none border-2 border-gray-200 rounded py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
        id="simultaneous-download"
        min="1"
        type="number"
        value="2"
      />
    </div>

    <div class="flex flex-row py-">
      <label class="settings-label" for="fix-broken-path"
        >Fix paths longer than 255 characters</label
      >
      <input
        class="h-6 w-6 form-checkbox text-gray-700 bg-gray-200"
        id="fix-broken-path"
        checked
        type="checkbox"
      />
    </div>
  </div>
</template>

<script>
const { dialog } = require("electron").remote;

export default {
  name: "Settings",
  methods: {
    openFolderDialog: function() {
      dialog
        .showOpenDialog({ properties: ["openDirectory"] })
        .then((data) => console.log(data.filePaths[0]));
    },
  },
};
</script>

<style>
.settings-label {
  @apply text-gray-700 text-sm font-bold inline-block my-auto mr-4;
}
</style>
