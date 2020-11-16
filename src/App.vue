<template>
  <div id="app" class="flex flex-col h-full">
    <InputUrlField />
    <div class="flex flex-row mb-auto">
      <SideBar class="w-1/8" />
      <router-view class="w-7/8" />
    </div>
    <BottomStatusBar class="h-10 sticky" />
  </div>
</template>

<script>
import InputUrlField from "@/components/InputUrlField";
import SideBar from "@/components/SideBar";
import BottomStatusBar from "@/components/BottomStatusBar";

export default {
  name: "App",
  components: {
    InputUrlField,
    SideBar,
    BottomStatusBar,
  },
};
</script>

<style scoped lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

div {
  user-select: none;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;F:abs($number: 0)
    }
  }
}
</style>
