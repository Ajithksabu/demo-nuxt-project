<template>
  <main class="flex-1">
    <div class="py-6">
      <div class="mx-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 md:px-8">
          <h1 class="text-2xl font-semibold text-gray-900">Employees</h1>
          <div class="flex justify-end mr-10">
            <button
              type="button"
              class="
                inline
                bg-white
                w-25
                px-2
                h-6
                mt-8
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
              Attatchments +
            </button>
            <button
              type="button"
              class="
                inline
                bg-white
                w-25
                px-2
                h-6
                mt-8
                ml-2
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
              Actions >
            </button>
          </div>
        </div>
      </div>
      <TabsView />      
    </div>
  </main>
</template>

<script>
import EmployeesGeneralDetails from "../../components/employeesGeneralDetails.vue";
import TabsView from "../../components/tabsView.vue";
export default {
  name: "EmployeeForm",
  layout: "app",
  components: {
    EmployeesGeneralDetails,
    TabsView,
  },
};
</script>