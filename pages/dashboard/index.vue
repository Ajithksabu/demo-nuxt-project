<template>
  <main class="flex-1">
    <div class="py-6">
      <div class="mx-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 md:px-8">
          <h1 class="text-2xl font-semibold text-gray-900">Employees</h1>
        </div>
        <nav
          class="
            relative
            w-full
            flex flex-wrap
            items-center
            justify-between
            py-3
            mx-2
            text-gray-500
            hover:text-gray-700
            focus:text-gray-700
            navbar navbar-expand-lg navbar-light
          "
        >
          <div
            class="
              container-fluid
              w-full
              flex flex-wrap
              items-center
              justify-between
              px-6
            "
          >
            <nav
              class="bg-grey-light rounded-md w-full"
              aria-label="breadcrumb"
            >
              <ol class="list-reset flex">
                <li>
                  <a href="#" class="text-gray-600 hover:text-gray-500"
                    >Dashboard</a
                  >
                </li>
                <li><span class="text-gray-500 mx-2">/</span></li>
                <li>
                  <a href="#" class="text-gray-400 hover:text-gray-300"
                    >Employees</a
                  >
                </li>
              </ol>
            </nav>
          </div>
        </nav>
      </div>
      <div class="max-w-7xl mx-auto px-4 sm:px-6 md:px-8">
        <EmployeeList />
      </div>
    </div>
  </main>
</template>

<script>
import EmployeeList from "../../components/employeeList.vue";
export default {
  name: "Home",
  layout: "app",
  components: {
    EmployeeList,
  },
};
</script>