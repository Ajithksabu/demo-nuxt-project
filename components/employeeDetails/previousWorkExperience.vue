<template>
  <div class="grow items-center justify-center px-5">
    <form action="#" method="POST">
      <div>
        <div class="bg-white py-6 px-4 space-y-6 sm:p-6">
          <!-- <h3 class="text-lg leading-6 font-medium text-gray-900">
            Previous Work Experience
          </h3> -->

          <div
            v-for="(field, index) in fieldList"
            v-bind:key="field.field1"
            class="grid grid-cols-6 gap-4"
          >
            <div>
              <label
                for="first-name"
                class="block text-sm font-medium text-gray-700"
                >{{ field.field1 }}</label
              >
              <input
                type="text"
                name="first-name"
                id="first-name"
                autocomplete="given-name"
                class="
                  mt-1
                  block
                  w-full
                  border border-gray-300
                  rounded-md
                  shadow-sm
                  py-2
                  px-3
                  focus:outline-none
                  focus:ring-indigo-500
                  focus:border-indigo-500
                  sm:text-sm
                "
              />
            </div>
            <div>
              <label
                for="first-name"
                class="block text-sm font-medium text-gray-700"
                >{{ field.field2 }}</label
              >
              <input
                type="text"
                name="first-name"
                id="first-name"
                autocomplete="given-name"
                class="
                  mt-1
                  block
                  w-full
                  border border-gray-300
                  rounded-md
                  shadow-sm
                  py-2
                  px-3
                  focus:outline-none
                  focus:ring-indigo-500
                  focus:border-indigo-500
                  sm:text-sm
                "
              />
            </div>
            <div>
              <label
                for="gender"
                class="block text-sm font-medium text-gray-700"
                >{{ field.field3 }}</label
              >
              <select
                id="country"
                name="country"
                autocomplete="country-name"
                class="
                  mt-1
                  block
                  w-full
                  bg-white
                  border border-gray-300
                  rounded-md
                  shadow-sm
                  py-2
                  px-3
                  focus:outline-none
                  focus:ring-indigo-500
                  focus:border-indigo-500
                  sm:text-sm
                "
              >
                <option>Select</option>
                <option>Female</option>
                <option>Male</option>
                <option>Others</option>
              </select>
            </div>
            <div>
              <label
                for="first-name"
                class="block text-sm font-medium text-gray-700"
                >{{ field.field4 }}</label
              >
              <input
                type="text"
                name="first-name"
                id="first-name"
                autocomplete="given-name"
                class="
                  mt-1
                  block
                  w-full
                  border border-gray-300
                  rounded-md
                  shadow-sm
                  py-2
                  px-3
                  focus:outline-none
                  focus:ring-indigo-500
                  focus:border-indigo-500
                  sm:text-sm
                "
                @click.prevent="openSalaryModal"
              />
            </div>
            <div>
              <button
                type="button"
                class="
                  inline
                  bg-white
                  w-20
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
                  focus:outline-none focus:ring-offset-2 focus:ring-gray-500
                "
                @click.prevent="addMore"
              >
                Add more
              </button>
              <button
                type="button"
                class="
                  inline
                  bg-white
                  w-20
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
                  focus:outline-none focus:ring-offset-2 focus:ring-gray-500
                "
                :class="{ hidden: fieldList.length < 2 || index === 0 }"
                @click.prevent="deleteRow"
              >
                Delete
              </button>
            </div>
          </div>
        </div>
        <div class="pt-5 mb-4">
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
    </form>
    <SalaryModal
      :openSalaryModal="openSalary"
      v-on:close-salary-modal="close"
      title="Salary card"
    />
  </div>
</template>

<script>
import SalaryModal from "../modals/salaryModal.vue";
export default {
  name: "PreviousWorkExperience",
  components: {
    SalaryModal,
  },
  data() {
    return {
      openSalary: false,
      fieldList: [
        {
          field1: "Company name",
          field2: "Designation",
          field3: "Experience",
          field4: "Salary",
        },
      ],
    };
  },
  methods: {
    openSalaryModal() {
      this.openSalary = true;
    },
    close() {
      this.openSalary = false;
    },
    addMore() {
      this.fieldList.unshift({
        field1: "Company name",
        field2: "Designation",
        field3: "Experience",
        field4: "Salary",
      });
    },
    deleteRow() {
      this.fieldList.pop();
    },
  },
};
</script>