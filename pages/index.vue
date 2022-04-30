<template>
  <div id="Start">
    <AppNavbar />
    <app-header />
    <AppContents />
  </div>
</template>

<script>
import AppHeader from "../components/AppHeader.vue";
import AppNavbar from "../components/AppNavbar.vue";
import AppContents from "../components/AppContents.vue";

export default {
  components: { AppHeader, AppContents, AppNavbar },
  name: "IndexPage",
};
</script>
