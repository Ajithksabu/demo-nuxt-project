<template>
  <main class="flex-1">
    <div class="py-6">
      <div class="mx-10">
        <div class="px-4 md:px-8">
          <h1 class="text-2xl font-semibold text-gray-900">Employees</h1>
        </div>
        <div class="flex justify-end">
          <button
            type="button"
            class="
              inline
              bg-white
              w-36
              px-2
              h-8
              mt-8
              mr-4
              border border-gray-300
              rounded-md
              shadow-sm
              text-sm
              leading-4
              font-medium
              text-gray-700
              hover:bg-gray-50
              focus:outline-none
              focus:ring-2
              focus:ring-offset-2
              focus:ring-gray-500
            "
            :class="{ hidden: tabNumber !== 1 }"
            @click.prevent="openModal"
          >
            Attatchments +
          </button>
          <select
            id="country"
            name="country"
            autocomplete="country-name"
            class="
              inline
              bg-white
              w-36
              px-2
              h-8
              mt-8
              mr-4
              border border-gray-300
              rounded-md
              shadow-sm
              text-sm
              leading-4
              font-medium
              text-gray-700
              hover:bg-gray-50
              focus:outline-none
              focus:ring-2
              focus:ring-offset-2
              focus:ring-gray-500
            "
          >
            <option disabled selected>Actions</option>
            <option>Appraisal</option>
            <option>Change status</option>
            <option>Staff exit</option>
          </select>
        </div>
      </div>
      <div class="mx-auto px-4 md:px-8">
        <TabsView @handle-tab="handleTab" />
      </div>
    </div>
    <AttatchmentModal
      :open="open"
      v-on:close="close"
      title="Add attatchments"
    />
  </main>
</template>

<script>
import EmployeesGeneralDetails from "../../components/employeesGeneralDetails.vue";
import TabsView from "../../components/tabsView.vue";
import AttatchmentModal from "../../components/modals/attatchmentModal.vue";
export default {
  name: "EmployeeForm",
  layout: "app",
  data() {
    return {
      open: false,
      tabNumber: 1,
    };
  },
  components: {
    EmployeesGeneralDetails,
    TabsView,
    AttatchmentModal,
  },
  methods: {
    openModal() {
      console.log("here");
      this.open = true;
    },
    close() {
      this.open = false;
    },
    handleTab(e) {
      this.tabNumber = e;
    },
  },
};
</script>