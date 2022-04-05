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

      <div class="ml-5">
        <div class="sm:hidden">
          <label for="tabs" class="sr-only">Select a tab</label>
          <select
            id="tabs"
            name="tabs"
            class="
              block
              w-full
              pl-3
              pr-10
              py-2
              text-base
              border-gray-300
              focus:outline-none focus:ring-indigo-500 focus:border-indigo-500
              sm:text-sm
              rounded-md
            "
          >
            <option v-for="tab in tabs" :key="tab.name" :selected="tab.current">
              {{ tab.name }}
            </option>
          </select>
        </div>
        <div class="hidden sm:block">
          <div class="border-b border-gray-200">
            <nav class="-mb-px flex space-x-8" aria-label="Tabs">              
              <a
                v-for="tab in tabs"
                :key="tab.name"
                :href="tab.href"
                :class="[
                  tab.current
                    ? 'border-indigo-500 text-indigo-600'
                    : 'border-transparent text-gray-500 hover:text-gray-700 hover:border-gray-300',
                  'whitespace-nowrap py-4 px-1 border-b-2 font-medium text-sm',
                ]"
                :aria-current="tab.current ? 'page' : undefined"
              >
                {{ tab.name }}
              </a>
            </nav>
          </div>
        </div>
      </div>

      <EmployeesGeneralDetails />
      <div class="pt-5">
        <div class="flex justify-end">
          <button
            type="button"
            class="
              bg-white
              py-2
              px-4
              border border-gray-300
              rounded-md
              shadow-sm
              text-sm
              font-medium
              text-gray-700
              hover:bg-gray-50
              focus:outline-none
              focus:ring-2
              focus:ring-offset-2
              focus:ring-indigo-500
            "
          >
            Cancel
          </button>
          <button
            type="submit"
            class="
              ml-3
              mr-5
              inline-flex
              justify-center
              py-2
              px-4
              border border-transparent
              shadow-sm
              text-sm
              font-medium
              rounded-md
              text-white
              bg-indigo-600
              hover:bg-indigo-700
              focus:outline-none
              focus:ring-2
              focus:ring-offset-2
              focus:ring-indigo-500
            "
          >
            Save
          </button>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import Sidebar from "../../components/sidebar.vue";
import SearchBar from "../../components/searchbar.vue";
import GeneralDetails from "../../components/employeeDetails/generalDetails.vue";
import ContactDetails from "../../components/employeeDetails/contactDetails.vue";
import EmploymentDetails from "../../components/employeeDetails/employmentDetails.vue";
import EducationalQualification from "../../components/employeeDetails/educationalQualification.vue";
import PreviousWorkExperience from "../../components/employeeDetails/previousWorkExperience.vue";
import CredentialDetails from "../../components/employeeDetails/credentialDetails.vue";
import EmployeesGeneralDetails from "../../components/employeesGeneralDetails.vue";
export default {
  name: "EmployeeForm",
  layout: "app",
  data() {
    return {
      tabs: [
        {
          name: "General details",
          href: "/employees",
        },
        {
          name: "Assets",
          href: "/about",
        },
        {
          name: "Appraisal",
          href: "/employees",
        },
      ],
    };
  },
  components: {
    Sidebar,
    SearchBar,
    EmployeesGeneralDetails,
  },
};
</script>