<template>
  <div>
    <div class="hidden md:block ml-5">
      <div>
        <nav class="-mb-px flex space-x-8" aria-label="Tabs">
          <a
            href="/employees"
            class="
              border-transparent
              text-gray-700
              whitespace-nowrap
              py-4
              px-1
              border-b-2
              font-medium
              text-sm
            "
            @click.prevent="toggleTabs(1)"
            v-bind:class="{
              'border-transparent text-gray-700 whitespace-nowrap py-4 px-1 border-b-2 font-medium text-sm':
                openTab !== 1,
              'border-red-500 border-b-4 ': openTab === 1,
            }"
          >
            General details
          </a>
          <a
            href="/about"
            class="
              border-transparent
              text-gray-700
              whitespace-nowrap
              py-4
              px-1
              border-b-2
              font-medium
              text-sm
            "
            @click.prevent="toggleTabs(2)"
            v-bind:class="{
              'border-transparent text-gray-700 whitespace-nowrap py-4 px-1 border-b-2 font-medium text-sm':
                openTab !== 2,
              'border-red-500 border-b-4': openTab === 2,
            }"
          >
            Assets
          </a>
        </nav>
      </div>
    </div>
    <div v-bind:class="{ hidden: openTab !== 1, block: openTab === 1 }">
      <EmployeesGeneralDetails />
    </div>
    <div v-bind:class="{ hidden: openTab !== 2, block: openTab === 2 }">
      <AssetsList />
    </div>
  </div>
</template>

<script>
import EmployeesGeneralDetails from "./employeesGeneralDetails.vue";
import AssetsList from "./assetsList.vue";
export default {
  name: "TabsView",
  data() {
    return {
      openTab: 1,
    };
  },
  components: {
    EmployeesGeneralDetails,
    AssetsList,
  },
  methods: {
    toggleTabs(tabNumber) {
      this.openTab = tabNumber;
      this.$emit("handle-tab", tabNumber);
    },
  },
};
</script>