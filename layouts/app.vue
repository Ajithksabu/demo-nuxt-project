<template>
  <div>
    <Sidebar />
    <div class="md:pl-64 flex flex-col flex-1">
      <SearchBar />
      <Nuxt />
    </div>
  </div>
</template>

<script>
import Sidebar from "../components/sidebar.vue"
import SearchBar from "../components/searchbar.vue";
export default {
  components: {
    Sidebar,
    SearchBar,
  },
};
</script>